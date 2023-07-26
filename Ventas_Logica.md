# Ventas

## Listado de Entidades

### clientes **(ED)**

- cliente_id **(PK)**
- nombre
- apellidos
- telefono **(UQ)**
- email **(UQ)**
- direccion
- codigo_postal
- ciudad
- pais **(FK)**

### productos **(ED|EC)**

- producto_id **(PK)**
- nombre
- descripcion
- foto
- precio
- cantidad

### ventas **(ED)**

- venta_id **(PK)**
- cliente_id **(FK)**
- fecha
- monto

### articulos_x_venta **(EP)**

- artiuclo_id **(PK)**
- venta_id **(FK)**
- producto_id **(FK)**
- cantidad

### paises **(EC)**

- pais_id **(PK)**
- nombre
- dominio **(UQ)**

## Relaciones

1. Un **cliente** tiene **pais** (_1-1_).
1. Un **cliente** genera **ventas** (_1-M_).
1. Una **venta** puede **articulos** (_1-M_).
1. Una **articulo** es un **producto** (_1-1_).

## Modelo Entidad Relacion Ventas.

![Modelo Venta](modeloVentaEntidadRelacion.drawio.png)

## Reglas de Negocio

### clientes

1. Crear un cliente.
1. Leer todos los clientes.
1. Leer un cliente en particular.
1. Actualizar un cliente.
1. Eliminar un cliente.

### productos

1. Crear un producto.
1. Leer todos los productos.
1. Leer un producto en particular.
1. Actualizar un producto.
1. Eliminar un producto.
1. Cada que haya una venta restar a la cantidad de prodictos disponibles, el número de artículos que se vendieron.

### ventas

1. Crea una venta.
1. Leer todas las ventas.
1. Leer una venta en particular. 
1. Leer todas las ventas de un cliente.
1. Leer todas las ventas de un producto.
1. Actualizar una venta.
1. Eliminar una venta.

### articulos_x_venta

1. Crear un articulo.
1. Leer todos los artículos.
1. Leer todos los artículos de una venta.
1. Leer todos los artículos de una producto.
1. Leer todos los artículos de una cliente.
1. Actualziar un artículo.

### paises

1. Crear un país.
1. Leer todos los paises.
1. Leer un país en particular.
1. Actulizar un país.
1. Eliminar un país.