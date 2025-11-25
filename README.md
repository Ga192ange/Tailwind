```bash
+---------------------+        +----------------------+        +----------------------+
|   CategoriaProducto | 1 ---- |      Producto        | ---- N |     Proveedor        |
+---------------------+        +----------------------+        +----------------------+
| id (PK)             |        | id (PK)              |        | id (PK)              |
| nombre              |        | nombre               |        | nombre               |
| descripcion         |        | categoria_id (FK)    |        | telefono             |
|                     |        | stock_minimo         |        | email                |
|                     |        | stock_maximo         |        | direccion            |
+---------------------+        | stock_actual         |        | ciudad               |
                               | fecha_vencimiento    |        | activo               |
                               +----------------------+        +----------------------+
                                         |
                                         | 1
                                         |
                                         N
                               +----------------------+
                               |     Movimiento       |
                               +----------------------+
                               | id (PK)              |
                               | producto_id (FK)     |
                               | tipo                 |
                               | cantidad             |
                               | fecha                |
                               +----------------------+
                                         |
                                         | 1
                                         |
                                         N
                               +----------------------+
                               |       Alerta         |
                               +----------------------+
                               | id (PK)              |
                               | producto_id (FK)     |
                               | movimiento_id (FK)   |
                               | nivel_stock          |
                               | estado               |
                               | tipo_alerta          |
                               | fecha                |
                               +----------------------+

```


  

