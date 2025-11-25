```bash
Tabla: CategoriaProducto
------------------------------------
id (PK)
nombre
descripcion


Tabla: Producto
------------------------------------
id (PK)
nombre
descripcion
categoria_id (FK → CategoriaProducto.id)
unidad_medida
stock_minimo
stock_maximo
stock_actual
precio_compra
precio_venta
fecha_vencimiento
activo
fecha_creacion
fecha_actualizacion


Tabla: HistorialPrecio
------------------------------------
id (PK)
producto_id (FK → Producto.id)
precio_anterior
nuevo_precio
fecha_cambio


```


  

