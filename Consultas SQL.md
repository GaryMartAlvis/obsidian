## Uniones
```sql
--Unión de tres tablas
SELECT 
    h.dwhdepagen AS cod_agencia,
    d.nombre AS nombre_cliente,
    e.dwhPlzDscp AS nombre_oficina
FROM dwhdep  AS h
INNER JOIN sfi_gbage AS d ON h.dwhdepcage = d.cage
INNER JOIN dwhplz AS e ON h.dwhdepagen = e.dwhPlzAgen
WHERE h.dwhdepnmod = 7;
```

## Formatos
```sql
-- Agrupación con formatos y uso de variables
DECLARE @day INT = 1;
SELECT
    FORMAT(SUM(prevision),   'N0', 'en-US') AS PREV,
    FORMAT(SUM(vigente),     'N0', 'en-US') AS VIG,
    FORMAT(SUM(ejecutado),   'N0', 'en-US') AS EJE,
    FORMAT((SUM(vigente)  +
            SUM(ejecutado)), 'N0', 'en-US') AS TOTAL_CART,
    FORMAT(MIN(fecha),          'dd-MM-yy') AS fecha_min
FROM Finanza_Score_Cartera_tbl
WHERE CONVERT(DATE, fecha) >= CONVERT(DATE, GETDATE() - @day);
```

## Búsqueda y reemplazo
```sql
-- Buscarv de estado de la cartera
SELECT 
	agencia, fecha, Oficial, 
	sum(TotalCartera) Monto, sum(prevision) Prev, count(*) Casos,  
	case
		when mora=0  or mora is null then  'Vig'
		when mora>=1 and mora<=30  then  'Atr'
		when estado=5 then 'Ven'
		when estado=6 then 'Eje'
		end as Estado2
FROM Finanza_Matriz_Cartera
WHERE convert(char(10),fecha,101) >= convert(char(10),getdate()-30,101)
GROUP BY agencia, fecha, Estado, Mora, codigooficial, Oficial
```
