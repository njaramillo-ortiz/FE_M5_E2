# FrontEnd - Módulo 5, Ejercicio 2

## Descripción del proyecto

Este proyecto consiste en una página web para un hospital ficticio, incluyendo sus diferentes servicios y personal médico.
Se continúa con el proyecto iniciado en el Módulo 4.

## Ejercicio

### Protección de Rutas con React Router DOM

Se utiliza `AuthContext` para proveer el contexto del usuario autenticado a cualquier script que lo solicite. El contexto retorna un objeto que incluye la referencia al usuario, las funciones `login` y `logout` y chequeos de autenticación: `isLogged`, `isDoctor` y `isAdmin`.
Se utliza `ProtectedRoute` para redirigir al usuario en caso de ingresar a una ruta no autorizada, y se utilizan los chequeos proporcionados en el contexto para ocultar los botones de la `Navbar` de manera acorde.

### Implementación de Autenticación de Usuarios y Roles

`AuthContext` implementa métodos de `login` y `logout` que se comunican con una base de datos simulada utilizando `json-server`. La base de datos almacena un usuario para cada rol (user, doctor y admin), con sus respectivas credenciales. Se incluye un componente `Login` que incluye inputs de usuario, contraseña y un botón para iniciar sesión, y un componenten `Logout` que muestra el nombre del usuario actual y un botón para cerrar sesión. Estos componentes se muestran dentro de `Navbar`, dependiendo de si existe información del usuario autenticado o no.

### Consumo de APIs Protegido con API Key y JWT



### Prevención de Vulnerabilidades Comunes



### Encriptación de Datos en el Front-End



## Instrucciones de uso

Requiere Node.js y npm instalados para su uso.
Desde la raíz del proyecto:
- Ejecutar el comando `npm install` para instalar las dependencias del proyecto.
- Ejecutar el comando `json-server db.json` para ejecutar la API simulada con base de datos.
- Ejecutar el comando `npm run dev` para ejecutar el proyecto.