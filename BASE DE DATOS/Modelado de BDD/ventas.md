# Sistema de ventas

> [!IMPORTANT]
> usaremos lo que ya aprendimos en el curso pasado por lo que estos son los pasos inciciales
> [Pasos inciales](../Diseño%20de%20BDD/readme.md)

## Listado de identidades

### Clientes **(ED)**de

- id **(PK)**
- nombre
- apellido
- mail
- numero
- codigo_postal
- direccion
- ciudad
- pais_id **(FK)**
- fecha_creacion
- fecha_actualizacion

### Pais **(EC)**

- id **(PK)**
- nombre

### Productos **(ED)**

- id **(PK)**
- nombre
- description
- cantidad
- precio
- img

### Ventas **(ED)**

- id **(PK)**
- productos_id **(FK)**
- cliente_id **(FK)**
- fecha
- monto

### ventas_productos **(ED)**

- id **(PK)**
- venta_id **(FK)**
- producto_id **(FK)**
- cantidad

### relacion

- **clientes** tiene un **pais** (1 a 1)
- **cliente** genera **(ventas)** (1 a M)
- **venta** tiene **articulos** (1 a M)
- **articulo** es un **producto** (1 a M)

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
1. Cada que haya una venta restar a la cantidad de productos disponibles, el número de artículos que se vendieron.

### ventas

1. Crear una venta.
1. Leer todas las ventas.
1. Leer una venta en particular.
1. Leer todas las ventas de un cliente.
1. Leer todas las ventas de un producto.
1. Actualizar una venta.
1. Eliminar una venta.

### articulos_x_venta

1. Crear un artículo.
1. Leer todos los artículos.
1. Leer un artículo en particular.
1. Leer todos los artículos de una venta.
1. Leer todos los artículos de un producto.
1. Leer todos los artículos de un cliente.
1. Actualizar un artículo.
1. Eliminar un artículo.

### paises

1. Crear un pais.
1. Leer todos los paises.
1. Leer un país en particular.
1. Actualizar un país.
1. Eliminar un país.
