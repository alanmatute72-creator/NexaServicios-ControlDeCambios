# 1. Actores del Sistema

Se identificaron **8 actores** a partir de las Historias de Usuario del documento aprobado. Se clasifican en **actores primarios** (interactúan directamente con el sistema para cumplir un objetivo) y **actores secundarios** (reciben efectos de las acciones de otros actores).

## 1.1 Actores primarios

Son quienes inician casos de uso y utilizan el sistema directamente para completar una tarea.

| Actor | Descripción del rol | HU relacionadas | Tipo |
|---------|-------------------|----------------|------|
| **Solicitante del cambio** | Empleado de cualquier área de Nexa Servicios que identifica la necesidad de un cambio operativo o tecnológico y lo registra formalmente en el sistema. Es el punto de entrada del proceso. | HU-01, HU-02, HU-03 | Primario |
| **Aprobador** | Responsable jerárquico o funcional que revisa, evalúa y decide si una solicitud de cambio puede avanzar hacia su implementación. Cuenta con autoridad formal para aprobar, rechazar o solicitar más información. | HU-04, HU-05, HU-06 | Primario |
| **Técnico de TI** | Especialista responsable de ejecutar técnicamente los cambios aprobados, registrar los resultados de la implementación y documentar los pasos seguidos en caso de reversa. | HU-07, HU-08, HU-09 | Primario |
| **Administrador del sistema** | Usuario con privilegios de configuración y administración. Gestiona usuarios, áreas, tipos de cambio y reglas de notificación del sistema. | HU-14, HU-15, HU-16, HU-22 | Primario |
| **Miembro del comité de cambios** | Integrante del comité institucional que revisa y vota sobre solicitudes clasificadas como de alto impacto antes de su aprobación final. Puede además registrar evaluaciones de riesgo. | HU-17, HU-18 | Primario |
| **Supervisor / Auditor** | Rol de supervisión que consulta el historial de cambios, revisa el estado general del proceso y descarga reportes para presentación a la gerencia. No modifica solicitudes. | HU-12, HU-13, HU-21 | Primario |

## 1.2 Actores secundarios

Son quienes no inician casos de uso pero reciben notificaciones, información o son afectados por las acciones de los actores primarios.

| Actor | Descripción del rol | HU relacionadas | Tipo |
|---------|-------------------|----------------|------|
| **Empleado afectado** | Colaborador cuya área o labor se ve impactada por un cambio aprobado. Recibe notificaciones automáticas del sistema y puede consultar materiales de capacitación. No inicia procesos por sí mismo. | HU-10, HU-11 | Secundario |
| **Usuario del sistema (genérico)** | Representa cualquier usuario autenticado, independientemente de su rol, con capacidad de iniciar sesión y consultar la trazabilidad de las solicitudes a las que tiene acceso. | HU-19, HU-20 | Secundario |

## Resumen de actores identificados

### Actores primarios (6)
1. Solicitante del cambio
2. Aprobador
3. Técnico de TI
4. Administrador del sistema
5. Miembro del comité de cambios
6. Supervisor / Auditor

### Actores secundarios (2)
1. Empleado afectado
2. Usuario del sistema (genérico)

**Total de actores identificados:** 8 actores.
