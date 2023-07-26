# Carreras

## Listado de Entidades

### carreras **(ED)**

- carrera_id **(PK)**
- nombre
- Tipo_carrera **(FK)**
- Fecha
- Tiempo
- Mejor_tiempo
- Altitud
- Lugar
- Pais **(FK)**
- Foto

## tipos_carreras **(EC)**

- tipos_carrera **(PK)**
- Descripcion
- Distancia **(UQ)**

## Paises **(EC)**

- pais_id **(PK)**
- Nombre 

## Relaciones

1. Una **carrera** _pertenece_ a un **tipo de carrera** (_1 a 1_).
1. Una **carrera** se  _corre_ eun un **país** (_1 a 1_).

## Diagramas

### Modelo Entidad- Relación.

! [Modelo Entidad - Relacion](./Modelo%20R-E.drawio.png)

### Modelo Relacional de la BD

! [Modelo Relacional BD](./CarrerasModeloRelacionalBD.drawio.png)