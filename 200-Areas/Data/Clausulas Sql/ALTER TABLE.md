[[ALTER TABLE]]

Modificar tabla.

```sql
--Adicionar nueva columna a la tabla
ALTER TABLE professors
ADD COLUMN university_shortname text;
```

```sql
--Eliminar columna de la tabla
ALTER TABLE name_table
DROP COLUMN column_name;
```

```sql
--Modificar el nombre de una columna
ALTER TABLE table_name
RENAME COLUMN old_name TO new_name;
```

```sql
-- Cambiar tipo de datos de una columna
ALTER TABLE professors
ALTER COLUMN firstname
TYPE VARCHAR(64);
```

# Convertir tipos UTILIZANDO una función

Si no quieres reservar demasiado espacio para una determinada columna `varchar`, puedes _truncar_ los valores antes de convertir su tipo.

```sql
-- Cambiar tipo conservando los primereos 16 caracteres de la columna
ALTER TABLE professors 
ALTER COLUMN firstname 
TYPE varchar(16)
USING SUBSTRING(firstname FROM 1 FOR 16)
```

## Convertir columna en llave primaria
```sql
ALTER TABLE name_table
ADD CONSTRAINT name_restriccion PRIMARY KEY(name_column)
```