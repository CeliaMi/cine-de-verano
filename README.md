## ¡Te damos la bienvenida al cine de verano🌞🩱 !

¡Hola coders! Bienvenidas a este nuevo proyecto donde crearemos una aplicación para disfrutar un cine de verano con recomendaciones de películas ideales para estos días calurosos.

El cine es una excusa para viajar, aprender y ponerse en la piel de otros a través de historias.

---

## ¿Qué aprenderemos en este proyecto?

- Crear una aplicación que pueda **leer**, **editar**, **guardar** y **eliminar** datos dinámicamente.
- Trabajar con **HTML**, **CSS** y **JavaScript**.
- Usar **json-server** para simular un servidor backend con un archivo JSON.

---

## Instalación y configuración desde cero

1. Inicializa un proyecto Node.js:

   ```bash
   npm init -y
   ```


2. Crea la siguiente estructura de carpetas y archivos:
```
    /server
    └── db.json
    /src
    ├── index.html
    └── services.js
    .gitignore
```
3. Crea un script para levantar el servidor JSON (json-server) y simular la API.

    ```json
        "scripts": {
            "test": "test",
            👉"api": "json-server --watch server/db.json"
        },
    ````

    Ahora escribe en tu terminal:
    ```bash
    npm run api
    ```

    verás como se levanta tu API que simula el servidor, ya tenemos un enlace al que hacer peticiones con Js 🐱‍🏍

       URL base: http://localhost:3000/movies

## ¡Manos a la obra! es el momento de Consumir la API con fetch

Ahora que tienes la API funcionando, toca conectar tu aplicación con ella. Usaremos JavaScript para hacer peticiones **fetch** que permitan realizar las operaciones básicas del CRUD:

- **Crear (POST):** enviar nuevas películas al servidor.
- **Leer (GET):** obtener la lista de películas para mostrar en la interfaz.
- **Actualizar (PUT/PATCH):** modificar detalles de alguna película.
- **Eliminar (DELETE):** borrar películas que ya no queramos mostrar.

Estas peticiones se harán desde el archivo `services.js` que creaste en la carpeta `/src`, utilizando la URL base:

