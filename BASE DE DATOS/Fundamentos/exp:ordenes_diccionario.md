# SISTEMA DE ORDENES

## Listado de entidades

### personal **(ED)**

- id_personal **(PK)**
- identificacion **(UQ)**
- nombre
- apellido
- numero
- mail
- id_rol **(FK)**

### roles **(EC)**

- id **(PK)**
- nombre
- descripcion

### clientes **(ED)**

- id_cliente **(PK)**
- identificacion **(UQ)**
- nombre
- apellido
- numero
- ciudad
- calle_1
- calle_2
- fecha_creacion
- fecha_actualizacion

### ordenes **(ED)**

- id_orden **(PK)**
- estado **(FK)**
- cliente_id **(FK)**
- personal_id **(FK)**
- description
- hora_preferencial
- fecha_visita
- fecha_creacion
- fecha_actualizacion

### motivo **(EC)**

- id **(PK)**
- Nombre

### estados **(EC)**

- id **(PK)**
- nombre

## Relaciones

1. Una **persona** tiene un **rol** y el **rol** pertene a varias **personas**

2. Una **orden** tiene un **estad0** ademas tiene un **motivo** pertenece a un **cliente** y la orden la cumple un **usario**

# Diagramas

# Modelo Relacional de la Base de Datos

![DIAGRAMA RELACIONAL](./ordes.drawio)

# Reglas de negocio
