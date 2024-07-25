[[INSERT INTO]]

Insertar información de una tabla a otra, hacer una copia de información.

```sql
INSERT INTO organizations
SELECT DISTINCT organization, organization_sector
FROM university_professors;
```

Inserción manual de datos a una tabla mediante código.
```sql
INSERT INTO table_name (columns_a, column_b)
VALUES ("value_a", "value_b");
```
