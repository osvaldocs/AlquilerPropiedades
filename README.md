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
| **Santiago Villa** | Líder Técnico | H3 y H4 — CRUD de Propietarios y Arrendatarios, DTOs, adaptadores, registro y listado de usuarios. |
| **Andrés Niebles** | Backend Dev | H2 y H5 — CRUD de Propiedades, validaciones, filtros y paginación. |
| **Yohan Exneider** | Backend Dev | H1 y H9 — Configuración base, arquitectura hexagonal, y test unitarios (Domain + Application). |
| **Pablo Campos** | API / Validaciones / Swagger / MapStruct | H6, H7 y H8 — Manejo global de errores, documentación Swagger y configuración/uso de MapStruct. |

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
| **H8** | Agregar MapStruct para conversión entre Entidades ↔ DTOs | Pablo | 3 | Crear mappers, configurar plugin y reemplazar conversiones manuales. |
| **H9** | **Test unitarios (Domain + Application)** | Yohan | 4 | Configurar junit + pruebas de servicios, puertos y validaciones. |
---

## 🧩 Integración de MapStruct

MapStruct permite mapear automáticamente entidades ↔ DTOs sin escribir código repetitivo.


---

## 🕓 Estimación por Sprint


| Sprint | Historias | Total SP | Objetivo |
|--------|-----------|-----------|----------|
| **Sprint 1** | H1 – H5 | 18 SP | Base + CRUD principales + usuarios + filtros básicos. |
| **Sprint 2** | H6 – H9 | 13 SP | Errores, documentación, MapStruct y test unitarios. |

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
