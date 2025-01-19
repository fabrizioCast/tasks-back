# Backend - Gestión de Tareas

Este es el backend del proyecto de gestión de tareas, construido con **NestJS** y **MySQL**. La API permite gestionar tareas con operaciones CRUD y autenticación de usuario mediante JWT.

## Instrucciones para instalar y ejecutar el proyecto

### Requisitos previos

- **Node.js**: Asegúrate de tener instalada la versión LTS de Node.js. Puedes verificarlo ejecutando `node -v`.
- **MySQL**: Necesitarás MySQL para la base de datos. Si no lo tienes instalado, puedes obtenerlo desde [aquí](https://dev.mysql.com/downloads/installer/).

### Pasos para instalar y ejecutar el backend

1. Clona este repositorio en tu máquina local:

   ```bash
   git clone https://github.com/tu_usuario/tu_repositorio.git
   cd tu_repositorio/backend
   ```

2. Instala las dependencias necesarias:

   ```bash
   npm install
   ```

3. Crea el archivo `.env` en la raíz del proyecto y configura las variables necesarias:

   ```env
   DATABASE_URL=mysql://usuario:contraseña@localhost:3306/tu_base_de_datos
   JWT_SECRET=tu_secreto_jwt
   ```

4. Ejecuta el servidor en modo desarrollo:

```bash
npm run start:dev
```

Esto levantará el servidor en `http://localhost:3000`.

### Endpoints principales

- **POST** `/auth/login`: Autenticación de usuario con JWT.
- **GET** `/tasks`: Obtener todas las tareas.
- **POST** `/tasks`: Crear una nueva tarea.
- **PUT** `/tasks/:id`: Actualizar una tarea.
- **DELETE** `/tasks/:id`: Eliminar una tarea.

### Estructura del proyecto

- `src/`: Contiene el código fuente.
- `src/auth/`: Módulos y estrategias de autenticación (JWT).
- `src/tasks/`: Módulos para la gestión de tareas (CRUD).
- `src/users/`: Módulos para la gestión de usuarios.
