# Sistema de ventas

> [!IMPORTANT]
> usaremos lo que ya aprendimos en el curso pasado por lo que estos son los pasos inciciales
> [Pasos inciales](../Diseño%20de%20BDD/readme.md)

## Listado de identidades

### Clientes **(ED)**

- id **(PK)**
- nombre
- apellido
- mail
- numero
- codigo_postal
- direccion
- ciudad
- pais_id **(FK)**

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
- priducto_id **(FK)**
- cantidad
