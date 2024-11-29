## 1. Título
Despliegue de Aplicación FrontEnd con Docker

## 2. Tiempo de duración
20 minutos

## 3. Fundamentos
Docker permite desplegar aplicaciones en contenedores, facilitando la configuración, distribución y escalabilidad de aplicaciones tanto en el frontend como en el backend. En este caso, se abordará el despliegue de una aplicación frontend construida con React utilizando Docker, al igual que se hizo con la aplicación backend en un proyecto anterior.

**Objetivos de la práctica:**
- Configurar un contenedor Docker para una aplicación React.
- Crear una imagen Docker para la aplicación frontend.
- Ejecutar la aplicación en un contenedor Docker y verificar su funcionamiento.

## 4. Conocimientos previos
- Uso básico de Docker.
- Conocimientos de cómo funciona React.
- Familiaridad con la creación de imágenes Docker.

## 5. Objetivos a alcanzar
- Crear un Dockerfile adecuado para una aplicación React.
- Construir una imagen Docker a partir del Dockerfile.
- Ejecutar la aplicación React en un contenedor Docker y probar su funcionamiento accediendo a la interfaz de usuario.

## 6. Equipo necesario
- Computadora con Docker instalado.
- Proyecto de aplicación frontend basado en React disponible, en este caso el repositorio `https://github.com/maguaman2/securityfe`.
- Conexión a Internet para descargar dependencias de Node.js.

## 7. Material de apoyo
- Documentación oficial de Docker: [https://docs.docker.com/](https://docs.docker.com/).
- Guía básica de React: [https://reactjs.org/docs/getting-started.html](https://reactjs.org/docs/getting-started.html).

## 8. Procedimiento

### Paso 1: Crear el Dockerfile para la aplicación React

En la raíz del proyecto, crear el siguiente archivo `Dockerfile`:
![image](https://github.com/user-attachments/assets/43c807f2-7346-495d-9722-5db2ade81697)

### Paso 2: Crear la imagen Docker
Con el Dockerfile creado, se debe construir la imagen Docker utilizando el siguiente comando:
`docker build -t myappfe:latest `

### Paso 3: Crear un contenedor a partir de la imagen y ejecutarlo
Una vez que la imagen se haya creado, ejecutamos un contenedor Docker con la imagen generada.
`docker run -d --network red_de_los_contenedores -p 3000:3000 myappfe`
Este comando ejecuta el contenedor en segundo plano

### Paso 4: Probar la aplicación
Abre un navegador web y accede a http://localhost:3000. La aplicación debería mostrar la lista de usuarios de la base de datos, lo que indica que está correctamente conectada con el backend y desplegada correctamente.
![image](https://github.com/user-attachments/assets/2196091d-fd2f-4d64-876f-d21f211ab2b1)

### 9. Resultados esperados

Contenedor de la aplicación frontend en React ejecutándose correctamente.
Acceso exitoso a la interfaz de usuario en http://localhost:3000, mostrando la lista de usuarios obtenida desde el backend.
La aplicación debe estar conectada con el backend y ser capaz de mostrar los mismos datos que se encuentran en http://localhost:8081/users.


### 10. Bibliografía
Merkel, D. (2014). Docker: Lightweight Linux Containers for Consistent Development and Deployment. Linux Journal, 2014(239), 2.
Kane, A. (2024). Docker in Action, Second Edition. Manning Publications.
Pahl, C., & Brogi, A. (2016). Cloud Container Technologies: A State-of-the-Art Review. IEEE Transactions on Cloud Computing, 5(4), 667-678.

