# Sistema Web de Gestión Académica Administrativa

Sistema web orientado a la administración de información académica y a la planificación de horarios escolares. Su propósito es facilitar al director la gestión de profesores, materias, grupos y disponibilidad, así como la generación, revisión y exportación de horarios.


## Funcionalidades previstas

- Administración de profesores, materias y grupos.
- Registro y consulta de disponibilidad docente.
- Generación de horarios a partir de restricciones académicas.
- Validación de conflictos entre asignaciones de profesores y grupos.
- Visualización y edición de horarios mediante una parrilla semanal.
- Exportación de reportes en PDF y Excel.
- Conservación de versiones de horarios.

El sistema está diseñado para que **el director sea el único usuario con acceso**.

## Arquitectura y tecnologías

El proyecto seguirá una arquitectura **cliente-servidor de tres capas**:

| Capa | Tecnologías previstas | Responsabilidad |
| --- | --- | --- |
| Presentación | React, TypeScript | Interfaz de administración |
| Lógica de negocio | Node.js, Express | API REST, autenticación y gestión de horarios |
| Datos | MySQL | Persistencia de la información académica |

La comunicación entre frontend y backend se realizará mediante una API REST con JSON sobre HTTPS en los entornos donde se configure TLS.

## Estructura del repositorio

```text
Gestor-de-horarios/
├── frontend/              # Interfaz de usuario
├── backend/               # API y lógica de negocio
├── database/
│   ├── estructura/        # Scripts de creación y modificación de tablas
│   └── datos-prueba/      # Registros ficticios para desarrollo
├── docs/                  # Documentación técnica y diagramas
└── README.md
```

Esta organización permite desarrollar el frontend, el backend y los scripts de MySQL dentro de un mismo repositorio, manteniendo separadas sus responsabilidades.

## Puesta en marcha

La instalación y ejecución local se documentarán cuando se incorporen los proyectos de React y Express, sus archivos `package.json` y la configuración de conexión a MySQL.

**Requisitos previstos:** Node.js, npm y MySQL. Las versiones compatibles se definirán durante la configuración inicial.

## Flujo de trabajo

La rama `main` se utiliza para mantener el código estable y cuenta con reglas de protección. Los cambios deben proponerse desde ramas de trabajo mediante Pull Requests.

Convención sugerida para nombres de ramas:

- `feature/nombre-funcionalidad` — Nuevas funcionalidades.
- `fix/nombre-correccion` — Correcciones.
- `chore/nombre-tarea` — Configuración y mantenimiento.

## Documentación

Los diagramas de arquitectura, el modelo entidad-relación, las decisiones de diseño y la documentación de la API se incorporarán a [`docs/`](docs/) conforme avance el proyecto.
