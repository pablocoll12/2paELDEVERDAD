# 2PA

2PA es una aplicación social basada en un mapa interactivo. Su objetivo es que las personas puedan descubrir lugares, indicar que quieren acudir a ellos solas o acompañadas y conectar con otras personas interesadas en el mismo sitio.

> **Estado del proyecto:** desarrollo inicial. Este README describe el producto que queremos construir; las funcionalidades mencionadas no deben interpretarse como ya implementadas.

## Cómo funciona

La aplicación distingue dos tipos de puntos en el mapa:

- **Puntos fijos:** lugares incorporados por el equipo de 2PA, como una discoteca. Permanecen disponibles en el mapa. Para solicitar asistencia, todos los participantes deben ser mayores de edad.
- **Puntos de interés temporales:** lugares propuestos por los usuarios para encontrar a otras personas o grupos interesados en acudir. Su duración y visibilidad se definirán en la especificación correspondiente.

Un usuario puede solicitar asistencia a un punto **por su cuenta** o **con integrantes de un grupo**. Tener un grupo creado no implica que todos sus miembros asistan: al hacer cada solicitud se eligen los participantes, y también debe ser posible acudir solo.

Si un punto temporal recibe mucho interés, el equipo de 2PA podrá estudiarlo y decidir si lo incorpora como punto fijo. Esta decisión no será automática.

## Perfiles y grupos

Cada usuario tendrá un perfil y podrá consultar por separado sus **seguidores** y las personas a las que **sigue**. Durante el registro podrá añadir una foto de perfil: será opcional, aunque la aplicación recomendará hacerlo.

Los usuarios podrán crear grupos de perfiles para organizar solicitudes de asistencia. La incorporación de miembros, el tamaño máximo de un grupo y las reglas para conectar con otras personas se concretarán antes de implementar estas funciones.

## Organización del repositorio

```text
2pa/
├── README.md
├── AGENTS.md
├── CLAUDE.md
├── .gitignore
├── docs/
│   └── constitution.md
├── specs/
│   └── 001-mapa-y-asistencias/
│       ├── spec.md
│       ├── plan.md
│       └── tasks.md
├── backend/
└── frontend/
```

`backend/` y `frontend/` contienen el código de la aplicación. Las carpetas y archivos de documentación SDD se incorporarán conforme se prepare el flujo de trabajo; su aparición en este esquema no significa que ya existan en el repositorio.

## Desarrollo guiado por especificaciones

Seguiremos el método de *Spec-Driven Development* (SDD) presentado en el [curso de MoureDev](https://www.youtube.com/watch?v=5HaOxAAA5qI) y su [repositorio de ejemplo](https://github.com/mouredev/hello-sdd):

1. **Constitución:** acordar principios y reglas del proyecto en `docs/constitution.md`.
2. **Especificación:** describir qué debe hacer una funcionalidad en `specs/NNN-nombre/spec.md`.
3. **Aclaración:** resolver las ambigüedades antes de diseñar la solución.
4. **Plan:** documentar cómo se implementará en `plan.md`.
5. **Tareas:** dividir el plan en pasos verificables en `tasks.md`.
6. **Implementación:** desarrollar una tarea cada vez.
7. **Validación:** comprobar los requisitos y actualizar la especificación cuando cambie el comportamiento esperado.

Claude Code y Codex trabajarán a partir de los mismos requisitos del repositorio. `AGENTS.md` contendrá las instrucciones comunes para los agentes y `CLAUDE.md` podrá referenciarlo.

## Decisiones pendientes

Antes de implementar las solicitudes de asistencia y las conexiones entre usuarios, debemos definir:

- Qué significa exactamente «solicitar asistencia» y cuándo se considera confirmada.
- Cómo se invita a los miembros de un grupo y cuál será el número máximo de integrantes.
- Cuánto dura un punto temporal y quién puede verlo.
- Qué ubicación se muestra y con qué precisión.
- Cómo se verifica la mayoría de edad para los puntos fijos.
- Cuándo y mediante qué consentimiento pueden conectar personas o grupos.

Estas decisiones se documentarán en las especificaciones antes de escribir el código correspondiente.

## Ramas y commits

`main` será la rama de integración. `dev_juan` y `dev_pablo` son las ramas personales de trabajo. Antes de abrir ramas para funcionalidades concretas o fusionar cambios, el equipo acordará desde qué rama parten y hacia cuál se dirige cada Pull Request.

Usaremos **Conventional Commits**:

| Prefijo | Uso |
| --- | --- |
| `feat:` | Nueva funcionalidad |
| `fix:` | Corrección de un error |
| `docs:` | Documentación |
| `test:` | Pruebas |
| `refactor:` | Reorganización del código sin cambiar su comportamiento |
| `chore:` | Mantenimiento y configuración |

Por ejemplo: `docs: add project README`.

## Puesta en marcha

Las instrucciones de instalación y ejecución del backend y del frontend se añadirán aquí después de comprobar las dependencias, variables de entorno y comandos reales del repositorio.# 2paELDEVERDAD
