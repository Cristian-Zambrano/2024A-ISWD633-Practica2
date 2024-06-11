## Esquema para el ejercicio
![Imagen](imagenes/esquema-ejercicio5.PNG)

### Crear la red
# COMPLETAR
```
docker network create wp -d bridge
```
### Crear el contenedor mysql a partir de la imagen mysql:8, configurar las variables de entorno necesarias
# COMPLETAR
```
docker run --name contenedorMYSQL --env-file=variablesEntorno.env --network wp -d mysql:8
```
### Crear el contenedor wordpress a partir de la imagen: wordpress, configurar las variables de entorno necesarias
# COMPLETAR
```
docker run --name contenedorWordPress --env-file=variablesEntorno.env --network wp -P -d wordpress
```
# Extra
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/c1791193-5f31-44b3-8fab-7c47f201ddc7)

De acuerdo con el trabajo realizado, en la el esquema de ejercicio el puerto a es: 9300

Ingresar desde el navegador al wordpress y finalizar la configuración de instalación.
# COLOCAR UNA CAPTURA DE LA CONFIGURACIÓN
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/82628a0a-6668-4dc9-b77b-534d021d5ad8)
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/62b12277-1b17-47e1-bbd5-52db94f915e2)
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/fa21334e-071d-419d-8d7e-0101f315f7a0)

Desde el panel de admin: cambiar el tema y crear una nueva publicación.
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress
# COLOCAR UNA CAPTURA DEL SITO EN DONDE SEA VISIBLE LA PUBLICACIÓN.
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/cef11ab0-1a96-4afc-8ed8-259367d173fa)
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/cb61d2b2-a95d-481d-981e-9ba2cd0a569f)
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/be67428f-d9df-46fa-8fab-ff735f50e9e7)

### Eliminar el contenedor wordpress
# COMPLETAR
```
docker rm contenedorWordPress -f
```
### Crear nuevamente el contenedor wordpress
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress

### ¿Qué ha sucedido, qué puede observar?
# COMPLETAR
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/c2a5f48f-c1a0-4a93-b6ac-cad90afc958d)
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-Practica2/assets/94475992/8a922f61-6099-49ec-a47b-3478c84a362e)
Se quedó guardada la página que estaba personalizando.






