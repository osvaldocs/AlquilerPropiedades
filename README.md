# 🏠 Proyecto: API de Alquiler de Propiedades

## 🎯 Objetivo
Desarrollar una **API REST** que gestione propiedades en alquiler y usuarios registrados, con operaciones CRUD, validaciones, paginación y documentación Swagger.  
Permite:
- Registrar y gestionar usuarios.
- Administrar propiedades, propietarios y arrendatarios.
- Consultar propiedades con filtros y paginación.

---

## 👥 Equipo y Roles

| Integrante | Rol | Responsabilidad Principal |
|-------------|------|----------------------------|
| **Santiago Villa** | Líder Técnico | Estructura del proyecto y configuración inicial (Spring Boot, H2). |
| **Andrés Niebles** | Backend Dev | CRUD y validaciones de **Propiedades**. |
| **Yohan Exneider** | Backend Dev | CRUD de **Propietarios** y **Arrendatarios**, paginación y filtros. |
| **Pablo Campos** | API / Validaciones / Swagger | Endpoints REST, validaciones (`@Valid`, `@NotBlank`, `@Email`) y documentación Swagger UI, registro de usuarios. |

---

## 🚀 Features Principales

1. **Gestión de Usuarios**
   - Registro de usuarios con validaciones (`@Email`, `@NotBlank`, `@Size`).
   - Listado de usuarios registrados.
   - Roles de usuario: Propietario / Arrendatario.

2. **Gestión de Propiedades**
   - CRUD completo.
   - Filtros por ciudad, precio o disponibilidad.
   - Paginación con `Pageable`.

3. **Gestión de Propietarios y Arrendatarios**
   - CRUD y validaciones (`@Email`, `@NotBlank`, `@Pattern`).

4. **Documentación y Manejo de Errores**
   - Swagger UI (`/swagger-ui/index.html`).
   - Manejo global de errores (`@ControllerAdvice`).

---

## 🧠 Historias de Usuario

| ID | Historia | Asignado a | Story Points | Descripción |
|----|-----------|-------------|---------------|--------------|
| **H1** | Configurar proyecto base (Spring Boot, Swagger, H2) | Santiago | 2 | Proyecto funcional con dependencias y estructura. |
| **H2** | CRUD Propiedades + Validaciones | Andrés | 5 | Endpoints REST para propiedades con validaciones. |
| **H3** | CRUD Propietarios y Arrendatarios | Yohan | 5 | Servicios y controladores con DTOs. |
| **H4** | Registro y listado de Usuarios | Santiago | 4 | Endpoints `/users/register` y `/users` con validaciones y roles. |
| **H5** | Paginación y filtros en Propiedades | Andrés | 3 | Soporte de `Pageable` y filtros por ciudad, precio, disponibilidad. |
| **H6** | Manejo global de errores | Pablo | 3 | `@ControllerAdvice` con mensajes claros. |
| **H7** | Documentación Swagger | Pablo | 3 | Swagger UI actualizado con todos los endpoints. |

---

## 🕓 Estimación de Esfuerzo

| Sprint | Historias | Total SP | Objetivo |
|--------|-----------|-----------|-----------|
| **Sprint 1** | H1 – H4 | 17 SP | API básica funcional con persistencia, validaciones y registro de usuarios. |
| **Sprint 2** | H5 – H7 | 7 SP | Paginación, filtros, manejo de errores y documentación final. |

---

## 🔄 Flujo de Trabajo (GitFlow)

- Rama principal: `main`  
- Rama de desarrollo: `develop`  
- Cada historia → rama `feature/<nombre>`  
- Merge a `develop` cuando la feature esté lista y funcionando.  

---

## 📄 Notas

- Todas las entidades usan **DTOs** para transferencia de datos.
- Validaciones aplicadas con `@Valid`, `@NotBlank`, `@Email`, `@Size`, `@Positive`, `@Pattern`.
- Swagger UI accesible en: `http://localhost:8080/swagger-ui/index.html`
- Roles de usuario: **Propietario** y **Arrendatario**.
- Registro de usuarios con endpoint `POST /users/register`.
