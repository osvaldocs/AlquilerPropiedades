# 🏠 Proyecto: API de Alquiler de Propiedades

## 🎯 Objetivo
Desarrollar una **API REST** que gestione propiedades en alquiler, con operaciones CRUD, validaciones, paginación y documentación Swagger.  
Permite registrar propiedades, propietarios y arrendatarios.

---

## 👥 Equipo y Roles

| Integrante | Rol | Responsabilidad Principal |
|-------------|------|----------------------------|
| **Santiago Villa** | Líder Técnico | Estructura del proyecto y configuración inicial (Spring Boot, H2). |
| **Andrés Niebles** | Backend Dev | CRUD y validaciones de **Propiedades**. |
| **Yohan Exneider** | Backend Dev | CRUD de **Propietarios** y **Arrendatarios**, paginación y filtros. |
| **Pablo Campos** | API / Validaciones / Swagger | Endpoints REST, validaciones (`@Valid`, `@NotBlank`, `@Email`) y documentación Swagger UI. |

---

## 🚀 Features Principales

1. **Gestión de Propiedades**
   - CRUD completo.
   - Filtros por ciudad, precio o disponibilidad.
   - Paginación con `Pageable`.

2. **Gestión de Propietarios**
   - CRUD y validaciones (`@Email`, `@NotBlank`).

3. **Gestión de Arrendatarios**
   - CRUD y validaciones de teléfono (`@Pattern`).

4. **Documentación y Manejo de Errores**
   - Swagger UI (`/swagger-ui/index.html`).
   - Manejo global de errores (`@ControllerAdvice`).

---

## 🧠 Historias de Usuario

| ID | Historia | Asignado a | Story Points | Descripción |
|----|-----------|-------------|---------------|--------------|
| **H1** | Configurar proyecto base (Spring Boot, Swagger, H2) | Santiago | 3 | Proyecto funcional con dependencias y estructura. |
| **H2** | CRUD Propiedades + Validaciones | Andrés | 5 | Endpoints REST para propiedades con validaciones. |
| **H3** | CRUD Propietarios y Arrendatarios | Yohan | 5 | Servicios y controladores con DTOs. |
| **H4** | Paginación y filtros en Propiedades | Andrés | 3 | Soporte de `Pageable` y filtros por ciudad, precio, disponibilidad. |
| **H5** | Manejo global de errores | Pablo | 2 | `@ControllerAdvice` con mensajes claros. |
| **H6** | Documentación Swagger | Pablo | 2 | Swagger UI actualizado con todos los endpoints. |

---

## 🕓 Estimación de Esfuerzo

| Sprint | Historias | Total SP | Objetivo |
|--------|-----------|-----------|-----------|
| **Sprint 1** | H1 – H3 | 13 SP | API básica funcional con persistencia y validaciones. |
| **Sprint 2** | H4 – H6 | 7 SP | Paginación, filtros, manejo de errores y documentación final. |

---

## 🔄 Flujo de Trabajo (GitFlow)

- Rama principal: `main`  
- Rama de desarrollo: `develop`  
- Cada historia → rama `feature/<nombre>`  
- Merge a `develop` cuando la feature esté lista y funcionando.  

---

## 📄 Notas

- Todas las entidades usan **DTOs** para transferencia de datos.
- Validaciones aplicadas con `@Valid`, `@NotBlank`, `@Email`, `@Positive`, `@Pattern`.
- Swagger UI accesible en: `http://localhost:8080/swagger-ui/index.html`
