
# Finanzas Personales - Backend

Este proyecto es el backend de una aplicación diseñada para gestionar finanzas personales. Permite el registro de ingresos, deudas y gastos, y realiza el cálculo automático del saldo restante. El backend está desarrollado en Node.js con Express y utiliza MongoDB como base de datos.

## Tabla de Contenidos

- [Tecnologías](#tecnologías)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Instalaciones Requeridas](#instalaciones-requeridas)
- [Configuración Inicial](#configuración-inicial)
- [Historias de Usuario](#historias-de-usuario)
- [Contribuciones](#contribuciones)

## Tecnologías

- **Node.js**
- **Express**
- **MongoDB** (Mongoose)
- **JWT** para autenticación
- **dotenv** para manejar variables de entorno

## Estructura del Proyecto

```
/src
  /controllers
    - userController.js
    - financeController.js
  /models
    - user.js
    - debt.js
    - income.js
    - expense.js
  /routes
    - userRoutes.js
    - financeRoutes.js
  /config
    - db.js
  - app.js
.env
```

## Instalaciones Requeridas

A continuación se indican los paquetes necesarios para instalar las dependencias del proyecto:

```bash
npm install express mongoose jsonwebtoken bcryptjs dotenv
```

## Configuración Inicial

1. Clona el repositorio.
   
2. Instala las dependencias del proyecto:

   ```bash
   npm install
   ```

3. Crea un archivo `.env` en la raíz del proyecto con las siguientes variables de entorno:

   ```bash
   PORT=3000
   MONGO_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/financeDB
   JWT_SECRET=supersecretkey
   ```

4. Ejecuta el servidor localmente:

   ```bash
   npm start
   ```

El servidor estará corriendo en `http://localhost:3000`.

## Historias de Usuario

### Historia 1.1: Configuración inicial del servidor Node.js con Express
- **Descripción**: Configuración del servidor Express básico.
- **Criterios de aceptación**:
  - El servidor Express debe estar corriendo y respondiendo en un puerto especificado.
  - El servidor debe mostrar un mensaje de bienvenida en la ruta base.

### Historia 1.2: Configuración de base de datos
- **Descripción**: Configurar MongoDB para almacenar datos de usuarios, ingresos, deudas y gastos.
- **Criterios de aceptación**:
  - La conexión entre Node.js y MongoDB debe estar establecida.
  - Los esquemas básicos para las colecciones deben estar definidos.

### Historia 1.3: Registro e inicio de sesión de usuarios
- **Descripción**: Permitir a los usuarios registrarse e iniciar sesión.
- **Criterios de aceptación**:
  - Rutas para registrar e iniciar sesión de usuarios.
  - Contraseñas encriptadas.
  - Tokens JWT para autenticación.

### Historia 1.4: CRUD de ingresos y deudas
- **Descripción**: Gestionar ingresos y deudas de los usuarios.
- **Criterios de aceptación**:
  - CRUD para ingresos y deudas.
  - Autenticación necesaria para realizar operaciones.

### Historia 1.5: Gestión de gastos diarios
- **Descripción**: Permitir a los usuarios gestionar sus gastos diarios.
- **Criterios de aceptación**:
  - CRUD para los gastos diarios.
  - Relación entre gastos y categorías.

### Historia 1.6: Cálculo del saldo restante
- **Descripción**: Calcular automáticamente el saldo restante.
- **Criterios de aceptación**:
  - El saldo restante se debe actualizar automáticamente.
  - Endpoint para consultar el saldo restante.

## Contribuciones

Si deseas contribuir al proyecto, por favor abre un **Pull Request** o crea un **Issue** para discutir los cambios que quieras realizar.

---

**Autor**: [Sebastian Diaz]
