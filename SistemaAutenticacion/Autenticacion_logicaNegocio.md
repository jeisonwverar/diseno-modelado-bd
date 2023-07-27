# Sistema de Autenticación

## Listado de Entidades

### usuarios **(ED)**

- usuario_id **(PK)**
- username **(UQ)**
- password
- email **(UQ)**
- nombre
- apellidos
- avatar
- activo
- fecha_creacion
- fecha_actualizacion

### roles **(EC)**

- rol_id **(PK)**
- nombre
- descripcion

### permisos **(EC)**

- permiso_id **(PK)**
- nombre
- descripcion

### roles_x_usuario **(EP)**

- rxu_id **(PK)**
- usuario_id **(FK)**
- rol_id **(FK)**

### permisos_x_roles **(EP)**

- pxr **(PK)**
- rol_id **(FK)**
- permiso_id **(FK)**

## Relaciones

1.  **usarios** tiene **roles** (_M-M_).
1.  **roles** tiene **permisos** (_M-M_).

## Modelo Relacional de la BD

![Modelo Relacional](sistemaAutenticacionMRelacional.drawio.png)

## Reglas de Negocio

### usuarios

1. Crear un usuario.
1. Leer todos los usuarios.
1. Leer un usario en particular.
1. Actualizar unusario.
1. Validar un usario.
1. Habilitar un usuario.
1. Inhabilitar un usuario.
1. Actualizar datos de un usuario.
1. Actualizar password de un usuario.
1. Eliminar un usuario.

### rol

1. Crear un rol.
1. Leer todos los roles.
1. Leer un rol en particular.
1. Actualizar un rol.
1. Eliminar un rol.

### permisos

1. Crear un permiso.
1. Leer todos los permisos.
1. Leer un permiso en particular.
1. Actualizar un permiso.
1. Eliminar un permiso.

### roles_x_usuario

1. Crear un rxu.
1. Leer todos los rxu.
1. Leer un rxu en particular.
1. Leer todos los rxu de un usuario.
1. Eliminar un rxu.

### permisos_x_roles

1. Crear un pxr.
1. Leer todos los pxr.
1. Leer un pxr en particular.
1. Leer todos los pxr de un roles.
1. Eliminar un pxr.
