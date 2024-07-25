[[CAST]]

Cláusula que cambia el tipo de dato de la columna.

```sql
--Cambiar el tipo de dato de una columna con valores tipo texto a numerico
SELECT temperature * CAST(wind_speed AS integer) AS wind_chill
FROM weather;
```

