[[Schema]]

Esquema de base de datos.

```sql
--Metadatos de base de datos TABLAS
SELECT column_name
FROM information_schema.tables 
WHERE table_schema = 'public';
```

```sql
--Metadatos de base de datos COLUMNAS
SELECT column_name, data_type 
FROM information_schema.columns 
WHERE table_name = 'university_professors' AND table_schema = 'public';
```