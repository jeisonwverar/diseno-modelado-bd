# Encuestas

## Listados de Entidades

### encuestas **(ED)**

- encuesta_id **(PK)**
- nombre
- descripcion
- imagen
- fecha
- encuestados

### preguntas **(ED)**

- pregunta_id **(PK)**
- encuesta_id **(FK)**
- pregunta

### respuestas **(ED)**

- respuesta_id **(PK)**
- pregunta_id **(FK)**
- respuesta
- es_correcta

### encuestados **(ED)**

- encuestado_id **(PK)**
- nombre
- apellidos
- edad
- email **(UQ)**

### resultados **(ED|EP)**

- resultado_id **(PK)**
- encuesta_id **(FK)**
- encuestado_id **(FK)**
- preguntas
- correctas

## Relaciones

1. una **encuesta** tiene **preguntas** (_1-M_).
1. una **pregunta** tiene **respuestas** (_1-M_).
1. una **pregunta** tiene **respuestas** (_1-M_).
1. un **encuestado** tiene **resultados** (_1-M_).

## Modelo Entidad Relacion

![Modelo-Relacional-Encuesta](EncuestasRelacionalDB.drawio%20(1).png)

## Reglas de Negocio

### encuestas

1. Crear una encuesta.
1. Leer todos los encuestas.
1. Leer un encuesta en particular.
1. Actualizar un encuesta.
1. Eliminar un encuesta.
1. Aumentar en 1 el valor del atributo encuestados  cada que un escuestado complete la encuesta.

### preguntas

1. Crea una pregunta.
1. Leer una pregunta.
1. Leer todas las preguntas.
1. Actualizar un pregunta.
1. Eliminar una pregunta.

###  respuestas

1. Crea una respuesta.
1. Leer una respuesta.
1. Leer todas las respuestas.
1. Actualizar un respuesta.
1. Eliminar una respuesta.

### encuestados

1. Crea un encuestado.
1. Leer un encuestado.
1. Leer todos los encuestados.
1. Actualizar un encuestado.
1. Eliminar un encuestado.

### resultado 

1. Crea una resultado.
1. Leer una resultado.
1. Leer todas las resultados.
1. Actualizar un resultado.
1. Eliminar una resultado.
1. antes de crear un encuestado en la entidad, verificar su email que no exista.
1. sacar el porcentaje de asertividad que tuvoel encuestado al contestar la encuesta.