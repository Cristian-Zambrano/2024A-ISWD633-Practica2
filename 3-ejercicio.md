### Crear contenedor de Postgres sin que exponga los puertos. Usar la imagen: postgres:11.21-alpine3.17
# COMPLETAR
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/983ddfaa-490d-4f44-ab6f-41695607403f)

### Crear un cliente de postgres. Usar la imagen: dpage/pgadmin4
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/7712992d-65b8-4e52-bdc7-af31caa02a50)


# COMPLETAR

La figura presenta el esquema creado en donde los puertos son:
- a: 80
- b: 80
- c: 5432

![Imagen](imagenes/esquema-ejercicio3.PNG)
# EXTRA
- Configurar variables de entorno necesarias
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/e8c17047-4c06-4b82-aa3e-d489f06f1834)
- Asignar los puertos descritos a los contenedores
- Consultar la ip de la imagen que contiene al postgres
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/25bc3a54-262a-44a9-b9d3-4cddaae6aa49)
## Desde el cliente
### Acceder desde el cliente al servidor postgres creado.
# COMPLETAR CON UNA CAPTURA DEL LOGIN
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/ba292c07-28cb-496a-ab66-79e6fb10f6a7)
# Extra 2
Luego de seguir lo descrito en Extra, realiza lo siguiente:
- Configura la conexión desde el cliente
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/f614877a-a262-4465-bf25-1ef069ad2071)
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/35cdfe61-2bfe-45d7-b909-bd5ef86f2c2a)
- Nota: no olvides que debes colocar las credenciales colocadas en el varEntorno.env
### Crear la base de datos info, y dentro de esa base la tabla personas, con id (serial) y nombre (varchar), agregar un par de registros en la tabla, obligatorio incluir su nombre.
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/db32c077-ffdb-4714-b6a1-c505c3994b76)
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/8ff8e3da-8d1e-4fbd-a561-1265a2f4220d)

## Desde el servidor postgresl
docker exec -it postgresContainer psql -U root -h localhost
### Acceder al servidor
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/2b1cece3-e50e-4d58-9dee-8ba01e74917e)

### Conectarse a la base de datos info
# COMPLETAR
\c info
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/1a5e9ed2-315f-4c6d-8f1c-9835ab35273c)

### Realizar un select *from personas
# AGREGAR UNA CAPTURA DE PANTALLA DEL RESULTADO
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/3cc48cdd-69d8-4844-8536-8ce10003200e)
