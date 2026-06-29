# E-commerce backend y pruebas de integración

Proyecto full stack educativo para practicar una API de e-commerce, autenticación y pruebas HTTP. El repositorio contiene un servidor Express con MongoDB y un cliente React separado.

## Funcionalidades

- Gestión de productos, carritos y usuarios.
- Registro, login, logout y consulta del usuario actual.
- Autenticación y autorización mediante middleware.
- Persistencia con MongoDB y patrón DAO/repository.
- Carga de archivos y envío de correo.
- Logging y manejo de errores.
- Generación de datos simulados.
- Vistas Handlebars y cliente React básico.
- Pruebas de sesiones, productos y carritos con Supertest.

## Stack

**Backend:** Node.js, Express, MongoDB, Mongoose y Handlebars.  
**Frontend:** React y Vite.  
**Testing:** Mocha, Chai y Supertest.

## Arquitectura

`src/routes` y `src/controllers` exponen la API; `src/repositories`, `src/daos` y `src/models` separan acceso a datos; `src/middleware` y `src/utils` contienen responsabilidades transversales. El cliente está en `client/ecomerce`.

## Configuración

Crear un `.env` local con las variables requeridas: `PORT`, `JWT_PRIVATE_KEY`, `JWT_SECRET`, `EMAIL`, `EMAIL_PASSWORD`, `GITHUB_CLIENT_ID`, `GITHUB_CLIENT_SECRET` y la conexión a MongoDB utilizada por la configuración.

## Ejecución

```bash
npm install
npm run dev
```

Pruebas: `npm test`. El cliente se instala y ejecuta desde `client/ecomerce`.

> No utilizar `src/config/development.env` para secretos reales. Las credenciales expuestas deben rotarse y migrarse a un `.env` ignorado por Git.