```sql
--Obtener fecha de servidor
SELECT *
FROM Finanza_Score_Cartera_tbl
WHERE CONVERT(DATE, fecha) >= CONVERT(DATE, GETDATE()-66);
```

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

