# Flujo de trabajo: Ramas, HU y Tareas en GitHub

Buenas equipo 👋  
Comparto el flujo de trabajo que vamos a usar para manejar ramas, historias de usuario y subdivisión en tareas dentro del repositorio y el tablero de GitHub Projects.

---

## 1. Rama principal del proyecto

El repositorio tiene estas ramas:

- **main** → Rama estable (solo se mergea lo probado y aprobado).  
- **develop** → Rama base donde trabajamos durante el sprint.

⚠️ Nadie trabaja directamente sobre `main`.

---

## 2. Crear ramas por Historia de Usuario (HU)

Cada integrante crea una branch por historia asignada:  

**Formato:**

feature/HX-nombre-corto

**Ejemplos:**

- `feature/H1-base-proyecto`
- `feature/H3-crud-propietarios`
- `feature/H8-mapstruct`

Cada historia se desarrolla solo dentro de su branch.

---

## 3. Subdividir la Historia de Usuario en tareas (si es necesario)

Si una HU es grande, en GitHub Projects podemos dividirla en **tasks** (issues más pequeños).

**Ejemplo para H1:**

- Task 1 – Crear entidades
- Task 2 – Crear repositorios
- Task 3 – Crear servicios
- Task 4 – Crear controladores
- Task 5 – Validaciones
- Task 6 – Tests

Las tasks se crean como issues normales, pero se vinculan a la HU principal usando:

- Projects → Add parent issue → H1  

O dentro del issue poniendo:

Parent: #<id de H1>


⚠️ **Importante:**  
Las tasks **NO necesitan llamarse “H1 – Task”**. Pueden llamarse simplemente:

Task 1 – Crear entidad


Mientras estén asociadas a H1, está perfecto.

---

## 4. Movimiento en el tablero (Kanban)

**Columnas:**

- **Backlog** → Ideas generales  
- **Ready** → Listas para empezar (el líder técnico las mueve)  
- **In Progress** → El dev está trabajando  
- **In Review** → Ya hay PR abierto hacia develop  
- **Done** → Mergeado y aprobado

---

## 5. Pull Requests

Cuando una historia o tarea está lista:

1. Crear PR hacia `develop`  
2. Solicitar mínimo 1 reviewer  
3. No mergear sin aprobación  
4. El líder técnico revisa integraciones grandes

---

## 6. Reglas rápidas

- Una rama por HU.  
- Una HU puede tener varias tasks.  
- Las tasks viven dentro del tablero y se linkean a la HU.  
- Cada PR debe mencionar qué issue resuelve:

