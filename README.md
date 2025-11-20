# 🏠 API de Alquiler de Propiedades

## 🧱 Arquitectura
El proyecto sigue una **Arquitectura Hexagonal (Ports & Adapters)**:
- **Domain**: Entidades y lógica del negocio.
- **Application**: Servicios, puertos, DTOs.
- **Infrastructure**: Controladores REST, repositorios JPA, Swagger, configuración.

Esto garantiza un sistema desacoplado, mantenible y escalable.

---

## 🎯 Objetivo del Proyecto
Desarrollar una **API REST** para gestionar propiedades en alquiler y usuarios.  
Incluye:
- CRUD completo.
- Validaciones con Bean Validation.
- Paginación y filtros.
- Manejo global de errores.
- Documentación con Swagger UI.
- Diseño desacoplado siguiendo arquitectura hexagonal.

---

## 👥 Equipo y Roles

| Integrante | Rol | Responsabilidad Principal |
|-----------|------|----------------------------|
| **Santiago Villa** | Líder Técnico | Configuración base, estructura hexagonal, H2, dependencias. |
| **Andrés Niebles** | Backend Dev | CRUD de Propiedades, validaciones, filtros y paginación. |
| **Yohan Exneider** | Backend Dev | CRUD de Propietarios y Arrendatarios, DTOs y servicios. |
| **Pablo Campos** | API / Validaciones / Swagger | Adaptadores REST, validaciones, documentación y registro de usuarios. |

---

## 🚀 Features Principales

### 🔹 Arquitectura Hexagonal
- Separación de Domain, Application e Infrastructure.
- Uso de interfaces (puertos) para servicios y repositorios.
- Adaptadores REST y JPA completamente desacoplados.

### 🔹 Gestión de Usuarios
- Registro con validaciones (`@Email`, `@NotBlank`, `@Size`).
- Listado de todos los usuarios.
- Roles: **Propietario** / **Arrendatario**.

### 🔹 Gestión de Propiedades
- CRUD completo.
- Filtros por ciudad, precio y disponibilidad.
- **Paginación con `Pageable`.**

### 🔹 Gestión de Propietarios y Arrendatarios
- CRUD completo.
- Validaciones con Bean Validation.

### 🔹 Documentación y Errores
- Swagger UI: `/swagger-ui/index.html`
- Manejo de errores con `@ControllerAdvice`.

---

## 🧠 Historias de Usuario

| ID | Historia | Asignado | SP | Descripción |
|----|----------|----------|----|-------------|
| **H1** | Configurar proyecto + Arquitectura hexagonal | Yohan | 3 | Base del proyecto, Domain/Application/Infrastructure. |
| **H2** | CRUD Propiedades + Validaciones | Andrés | 4 | Endpoints REST usando puertos y servicios. |
| **H3** | CRUD Propietarios y Arrendatarios | Santiago | 4 | Servicios, DTOs y adaptadores. |
| **H4** | Registro y listado de usuarios | Santiago | 4 | Endpoints `/users/register` y `/users`. |
| **H5** | Paginación y filtros | Andrés | 3 | Implementar `Pageable` + filtros combinados. |
| **H6** | Manejo global de errores | Pablo | 3 | DTOs de error y `@ControllerAdvice`. |
| **H7** | Documentación Swagger | Pablo | 3 | Anotaciones, tags, esquemas. |

---

## 🕓 Estimación por Sprint

| Sprint | Historias | Total SP | Objetivo |
|--------|-----------|-----------|----------|
| **Sprint 1** | H1 – H4 | 15 SP | Base + CRUD principales + usuarios. |
| **Sprint 2** | H5 – H7 | 9 SP | Filtros, paginación, documentación y errores. |

---

## 🔄 Flujo de Trabajo (GitFlow)

- `main` → versión estable  
- `develop` → integración  
- Cada historia → rama `feature/<nombre>`  
- PR hacia `develop` → revisión y merge  

---

## 📄 Notas Técnicas

- Todas las entidades usan **DTOs** para transferencia de datos.
- Validaciones aplicadas con:  
  `@Valid`, `@NotBlank`, `@Email`, `@Size`, `@Positive`, `@Pattern`.
- Swagger UI:  
  `http://localhost:8080/swagger-ui/index.html`
- Roles soportados: **Propietario** y **Arrendatario**.

---
