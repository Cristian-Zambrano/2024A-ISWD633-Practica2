# Variables de Entorno
### ¿Qué son las variables de entorno
# COMPLETAR
# Es un valor dinámico que el sistema operativo y otros programas pueden utilizar para determinar información específica de el computador.
### Para crear un contenedor con variables de entorno

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```

### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.

# COMPLETAR
```
docker run -d --name nginxContainer -e username=admin -e role=admin -p 80:80 nginx

```
# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/59ac1e17-4908-4c57-bb35-a8ad20ae848a)

### Crear un contenedor con mysql:8 , mapear todos los puertos
# COMPLETAR
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/cae79fca-4811-4f0d-bad2-911040899abe)

### ¿El contenedor se está ejecutando?
# COMPLETAR
# No se está ejecutando el contenedor "mysqlContainer"
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/be7342f1-d6aa-4c90-81f8-7054d9f1fe84)

### Identificar el problema
# COMPLETAR
# La configuración de algunas variables que necesita la imagen no están definidas.
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/54d5751a-89f5-4b9b-aa77-8734506dce9e)

### Eliminar el contenedor creado con mysql:8 
# COMPLETAR
```
docker rm msqlContainer
```
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/d3b99d08-9e9f-4dc3-b73d-06d4b612741e)


### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

Previo a esto es necesario crear el archivo y colocar las variables en un archivo, **.env** se ha convertido en una convención estándar, pero también es posible usar cualquier extensión como **.txt**.
```
docker run -d --name <nombre contenedor> --env-file=<nombreArchivo>.<extensión> <nombre imagen>
```
**Considerar**
Es necesario especificar la ruta absoluta del archivo si este se encuentra en una ubicación diferente a la que estás ejecutando el comando docker run.

### Crear un contenedor con mysql:8 , mapear todos los puertos y configurar las variables de entorno mediante un archivo
# COMPLETAR
docker run -d --name msqlContainer --env-file=varEntorno.env -P mysql:8
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/14824930-5eab-46e9-8119-439aad323c01)



# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR 
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/96269d71-7bea-4c92-9987-dcf5afa405f6)
### ¿Qué bases de datos existen en el contenedor creado?
# COMPLETAR
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/be54c3ef-9fae-4796-a539-2c55e3e8510b)
