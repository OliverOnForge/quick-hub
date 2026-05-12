
# Conventional Commits

El commit debe responder las preguntas ¿Qué? y ¿Por qué? se hizo el cambio. Se conforma de la sig. manera:

- [Conventional Commits](#conventional-commits)
  - [Encabezado del Commit](#encabezado-del-commit)
  - [Cuerpo del Commit](#cuerpo-del-commit)

## Encabezado del Commit

[Tipo-de-commit] [Alcance]: [resumen-del-cambio]

> Obligatorio
> Máximo de 50 caracteres. (Si es muy largo debería fraccionarse en varios commits más pequeños).
> Sin signos de puntucaion.

- **Tipo-de-commit** Indica el propósito del cambio:

  - feat: Una nueva característica para el usuario.
  - fix: Arregla un bug que afecta al usuario.
  - refactor: Refactorización del código, como cambios de nombre de variables o funciones.
  - docs: Cambios en la documentación.
  - style: Cambios de formato (espacios, tabulaciones, puntos y coma) que no afectan al usuario.
  - test: Añade o refactoriza pruebas.
  - perf: Cambios que mejoran el rendimiento.
  - build: Cambios en el sistema de build, tareas de despliegue o instalación.
  - ci: Cambios en la integración continua.
  - chore: Mantenimiento de código regular.

- **Alcance** Indica que parte del proyecto fue afectada por el commit (Backend, database, readme, ui, archivo.txt)

- **Descripción-corta-del-cambio** Una explicación clara y directa de los cambios realizados (Mejorar la lógica del carrito de compras, Añadir pruebas unitarias,  Corregir error de inicio de sesión).

## Cuerpo del Commit

- Se usa para explicar los cambios realizados (a detalle) y el ¿Por qué?
- Se recomienda usar 72 caracteres (redaccion libre)
- Es recomendable añadir una referencia al problema como: Soluciona: "Error: 123-A".