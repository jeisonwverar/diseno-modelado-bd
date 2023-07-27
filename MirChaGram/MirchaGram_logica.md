# Modelado de Red social MirchaGram

## Lista de Entidades

### posts **(ED)**

- post_id  **(PK)**
- post_date
- plot
- photo
- user **(FK)**

### user **(ED)**

- user **(PK)**
- user_date 
- user_name
- email **(UQ)**
- password
- phone **(UQ)**
- bio
- web
- birthdate
- genre
- country **(FK)**

### comments **(ED|EP)**

- comments_id **(PK)**
- comment_date
- comment
- post_id **(FK)**
- user **(FK)**

### hearts **(ED|EP)**

- heart_id **(PK)**
- heart_Date
- post_id **(FK)**
- user **(FK)**

### follows **(ED)**

- follow_id **(PK)**
- follow_date
- follow_user 
- user **(FK)**

### counties **(EC)**

- country_id **(PK)**
- country_name 


## Relaciones

## Modelo Entidad

## Reglas de negocio