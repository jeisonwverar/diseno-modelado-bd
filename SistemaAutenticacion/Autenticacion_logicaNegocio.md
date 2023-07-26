# Sistema de Autenticación

## Listado de Entidades

### usuarios **(ED)**
-usuario_id **(PK)**
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

### permisos  **(EC)**

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

