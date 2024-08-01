[RESTRICCIONES SQL]

En SQL, `ADD CONSTRAINT` se utiliza para agregar una nueva restricción a una tabla existente. Las restricciones son reglas aplicadas a los datos en una tabla para asegurar la integridad y la validez de los datos.

### PRIMARY KEY
```sql
-- Restricción de clave primaria aplicada a una columna
ALTER TABLE name_table
ADD CONSTRAINT name_restriccion PRIMARY KEY(name_column);

-- Eliminar restricción
ALTER TABLE name_table
DROP CONSTRAINT name_restriccion;

-- Crear una nueva columna con la restricción de clave primaria
ALTER TABLE name_table
ADD COLUMN id serial PRIMARY KEY; 
--id: nombre de la columna | serial: instrucción de secuencia serial de la column
```

### FOREIGN KEY
### UNIQUE
### CHECK
### NOT NULL