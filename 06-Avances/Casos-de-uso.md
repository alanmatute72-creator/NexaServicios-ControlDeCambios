# 2. Casos de Uso

Se derivaron 14 casos de uso a partir de los requisitos funcionales y las historias de usuario del documento aprobado. Cada caso de uso representa una interacción completa entre un actor y el sistema para lograr un objetivo de negocio. No se incluyeron casos de uso sin sustento en el documento base.

## CU-01 — Registrar solicitud de cambio

| Campo                       | Descripción                                                                                                                                                                                                                                                                       |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Código**                  | CU-01                                                                                                                                                                                                                                                                             |
| **Nombre**                  | Registrar solicitud de cambio                                                                                                                                                                                                                                                     |
| **Objetivo**                | Permitir al solicitante documentar formalmente un cambio requerido con todos sus datos de soporte.                                                                                                                                                                                |
| **Actor principal**         | Solicitante del cambio                                                                                                                                                                                                                                                            |
| **Descripción breve**       | El solicitante accede al formulario de nueva solicitud, completa los campos obligatorios (título, descripción, justificación, área afectada y fecha esperada), adjunta los archivos requeridos y envía la solicitud. El sistema genera un radicado único y notifica la recepción. |
| **Requisitos relacionados** | RF-01, RF-02, RF-03                                                                                                                                                                                                                                                               |
| **Reglas de negocio**       | RN-01, RN-02, RN-11                                                                                                                                                                                                                                                               |

---

## CU-02 — Consultar estado de solicitudes propias

| Campo                       | Descripción                                                                                                                                                                  |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Código**                  | CU-02                                                                                                                                                                        |
| **Nombre**                  | Consultar estado de solicitudes propias                                                                                                                                      |
| **Objetivo**                | Permitir al solicitante hacer seguimiento al estado actual de todas las solicitudes que ha registrado.                                                                       |
| **Actor principal**         | Solicitante del cambio                                                                                                                                                       |
| **Descripción breve**       | El solicitante accede a su panel de solicitudes y visualiza el listado con el estado actual de cada una. Puede seleccionar cualquier solicitud para ver su detalle completo. |
| **Requisitos relacionados** | RF-04                                                                                                                                                                        |
| **Reglas de negocio**       | —                                                                                                                                                                            |

---

## CU-03 — Revisar solicitudes pendientes de aprobación

| Campo                       | Descripción                                                                                                                                                                           |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Código**                  | CU-03                                                                                                                                                                                 |
| **Nombre**                  | Revisar solicitudes pendientes de aprobación                                                                                                                                          |
| **Objetivo**                | Permitir al aprobador visualizar y priorizar las solicitudes que requieren su atención.                                                                                               |
| **Actor principal**         | Aprobador                                                                                                                                                                             |
| **Descripción breve**       | El aprobador accede a su bandeja de solicitudes pendientes filtradas por su área. El sistema resalta las solicitudes con más de 3 días sin movimiento para facilitar la priorización. |
| **Requisitos relacionados** | RF-05, RF-06                                                                                                                                                                          |
| **Reglas de negocio**       | —                                                                                                                                                                                     |

---

## CU-04 — Aprobar o rechazar una solicitud de cambio

| Campo                       | Descripción                                                                                                                                                                                                                              |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Código**                  | CU-04                                                                                                                                                                                                                                    |
| **Nombre**                  | Aprobar o rechazar una solicitud de cambio                                                                                                                                                                                               |
| **Objetivo**                | Permitir al aprobador tomar una decisión formal sobre una solicitud, dejando evidencia escrita de la razón.                                                                                                                              |
| **Actor principal**         | Aprobador                                                                                                                                                                                                                                |
| **Descripción breve**       | El aprobador revisa la solicitud, consulta la justificación y archivos adjuntos, escribe un comentario obligatorio y selecciona Aprobar o Rechazar. El sistema registra la decisión con nombre, fecha y hora, y notifica al solicitante. |
| **Requisitos relacionados** | RF-07, RF-08                                                                                                                                                                                                                             |
| **Reglas de negocio**       | RN-03, RN-04                                                                                                                                                                                                                             |

---

## CU-05 — Solicitar información adicional al solicitante

| Campo                       | Descripción                                                                                                                                                                                                                                                                                                              |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Código**                  | CU-05                                                                                                                                                                                                                                                                                                                    |
| **Nombre**                  | Solicitar información adicional al solicitante                                                                                                                                                                                                                                                                           |
| **Objetivo**                | Permitir al aprobador requerir datos adicionales sin cerrar ni rechazar la solicitud.                                                                                                                                                                                                                                    |
| **Actor principal**         | Aprobador                                                                                                                                                                                                                                                                                                                |
| **Descripción breve**       | El aprobador identifica que la solicitud no tiene información suficiente para tomar una decisión. Cambia el estado a Pendiente de información y especifica qué necesita. El sistema notifica al solicitante, quien puede responder y adjuntar archivos. Al responder, la solicitud regresa automáticamente al aprobador. |
| **Requisitos relacionados** | RF-09, RF-10                                                                                                                                                                                                                                                                                                             |
| **Reglas de negocio**       | RN-05                                                                                                                                                                                                                                                                                                                    |

---

## CU-06 — Visualizar cambios aprobados para implementación

| Campo                       | Descripción                                                                                                                                                   |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Código**                  | CU-06                                                                                                                                                         |
| **Nombre**                  | Visualizar cambios aprobados para implementación                                                                                                              |
| **Objetivo**                | Permitir al técnico de TI identificar y priorizar los cambios que debe ejecutar.                                                                              |
| **Actor principal**         | Técnico de TI                                                                                                                                                 |
| **Descripción breve**       | El técnico accede a su panel de trabajo y visualiza únicamente las solicitudes en estado Aprobada asignadas a su área, ordenadas por fecha de implementación. |
| **Requisitos relacionados** | RF-11                                                                                                                                                         |
| **Reglas de negocio**       | —                                                                                                                                                             |

---

## CU-07 — Registrar resultado de implementación

| Campo                       | Descripción                                                                                                                                                                                                                                   |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Código**                  | CU-07                                                                                                                                                                                                                                         |
| **Nombre**                  | Registrar resultado de implementación                                                                                                                                                                                                         |
| **Objetivo**                | Permitir al técnico documentar formalmente el resultado de ejecutar un cambio aprobado.                                                                                                                                                       |
| **Actor principal**         | Técnico de TI                                                                                                                                                                                                                                 |
| **Descripción breve**       | El técnico ejecuta el cambio y registra el resultado seleccionando entre Exitosa, Parcial o Fallida, con un comentario descriptivo obligatorio. El sistema actualiza el estado de la solicitud según el resultado y notifica a los afectados. |
| **Requisitos relacionados** | RF-12, RF-13, RF-14, RF-15                                                                                                                                                                                                                    |
| **Reglas de negocio**       | —                                                                                                                                                                                                                                             |

---

## CU-08 — Registrar plan de reversa

| Campo                       | Descripción                                                                                                                                                                                                |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Código**                  | CU-08                                                                                                                                                                                                      |
| **Nombre**                  | Registrar plan de reversa                                                                                                                                                                                  |
| **Objetivo**                | Permitir al técnico documentar los pasos seguidos para deshacer un cambio que falló o quedó incompleto.                                                                                                    |
| **Actor principal**         | Técnico de TI                                                                                                                                                                                              |
| **Descripción breve**       | Ante un resultado Fallida o desde el estado En revisión técnica, el técnico accede al formulario de reversa y documenta paso a paso las acciones realizadas para restaurar el estado anterior del sistema. |
| **Requisitos relacionados** | RF-16                                                                                                                                                                                                      |
| **Reglas de negocio**       | —                                                                                                                                                                                                          |

---

## CU-09 — Recibir y consultar notificaciones de cambios

| Campo                       | Descripción                                                                                                                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Código**                  | CU-09                                                                                                                                                                                                   |
| **Nombre**                  | Recibir y consultar notificaciones de cambios                                                                                                                                                           |
| **Objetivo**                | Permitir al empleado afectado mantenerse informado sobre los cambios que impactan su área.                                                                                                              |
| **Actor principal**         | Empleado afectado                                                                                                                                                                                       |
| **Descripción breve**       | El empleado recibe notificaciones automáticas cuando un cambio de su área es aprobado, falla o se revierte. Puede acceder al detalle del cambio y descargar los materiales de capacitación disponibles. |
| **Requisitos relacionados** | RF-17, RF-18                                                                                                                                                                                            |
| **Reglas de negocio**       | —                                                                                                                                                                                                       |

---

## CU-10 — Consultar historial de cambios

| Campo                       | Descripción                                                                                                                                                                                      |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Código**                  | CU-10                                                                                                                                                                                            |
| **Nombre**                  | Consultar historial de cambios                                                                                                                                                                   |
| **Objetivo**                | Permitir al supervisor revisar y exportar el registro completo e inmutable de todos los cambios realizados.                                                                                      |
| **Actor principal**         | Supervisor / Auditor                                                                                                                                                                             |
| **Descripción breve**       | El supervisor accede al módulo de historial, aplica filtros por período, área, estado o aprobador, y consulta el flujo completo de cada solicitud. Puede exportar los resultados en PDF o Excel. |
| **Requisitos relacionados** | RF-19, RF-20                                                                                                                                                                                     |
| **Reglas de negocio**       | RN-09                                                                                                                                                                                            |

---

## CU-11 — Visualizar panel de resumen y alertas

| Campo                       | Descripción                                                                                                                                                               |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Código**                  | CU-11                                                                                                                                                                     |
| **Nombre**                  | Visualizar panel de resumen y alertas                                                                                                                                     |
| **Objetivo**                | Permitir al supervisor monitorear el estado general del proceso e identificar solicitudes represadas.                                                                     |
| **Actor principal**         | Supervisor / Auditor                                                                                                                                                      |
| **Descripción breve**       | El supervisor accede al panel de indicadores que muestra contadores por estado. El sistema genera alertas visibles para las solicitudes con más de 5 días sin movimiento. |
| **Requisitos relacionados** | RF-21, RF-22                                                                                                                                                              |
| **Reglas de negocio**       | —                                                                                                                                                                         |

---

## CU-12 — Gestionar usuarios del sistema

| Campo                       | Descripción                                                                                                                                                                                                                                          |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Código**                  | CU-12                                                                                                                                                                                                                                                |
| **Nombre**                  | Gestionar usuarios del sistema                                                                                                                                                                                                                       |
| **Objetivo**                | Permitir al administrador crear, modificar y desactivar cuentas de usuario manteniendo la integridad del historial.                                                                                                                                  |
| **Actor principal**         | Administrador del sistema                                                                                                                                                                                                                            |
| **Descripción breve**       | El administrador puede crear nuevos usuarios asignando nombre, correo, área y rol. Puede modificar la información de usuarios existentes sin afectar su historial. Puede desactivar cuentas conservando toda la trazabilidad de acciones anteriores. |
| **Requisitos relacionados** | RF-23, RF-33, RF-34                                                                                                                                                                                                                                  |
| **Reglas de negocio**       | RN-10                                                                                                                                                                                                                                                |

---

## CU-13 — Configurar áreas, categorías y notificaciones

| Campo                       | Descripción                                                                                                                                                                                    |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Código**                  | CU-13                                                                                                                                                                                          |
| **Nombre**                  | Configurar áreas, categorías y notificaciones                                                                                                                                                  |
| **Objetivo**                | Permitir al administrador personalizar la estructura organizacional y las reglas de comunicación del sistema.                                                                                  |
| **Actor principal**         | Administrador del sistema                                                                                                                                                                      |
| **Descripción breve**       | El administrador puede crear, modificar o desactivar áreas y tipos de cambio del sistema. También puede configurar qué roles reciben notificaciones en cada cambio de estado de una solicitud. |
| **Requisitos relacionados** | RF-24, RF-25                                                                                                                                                                                   |
| **Reglas de negocio**       | —                                                                                                                                                                                              |

---

## CU-14 — Revisar, evaluar y votar solicitudes de alto impacto

| Campo                       | Descripción                                                                                                                                                                                                                                                                                                                                              |
| --------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Código**                  | CU-14                                                                                                                                                                                                                                                                                                                                                    |
| **Nombre**                  | Revisar, evaluar y votar solicitudes de alto impacto                                                                                                                                                                                                                                                                                                     |
| **Objetivo**                | Permitir al comité de cambios analizar, registrar riesgos y votar sobre solicitudes que pueden causar problemas graves.                                                                                                                                                                                                                                  |
| **Actor principal**         | Miembro del comité de cambios                                                                                                                                                                                                                                                                                                                            |
| **Descripción breve**       | El comité recibe automáticamente las solicitudes clasificadas como de alto impacto. Cada miembro puede leer la solicitud, registrar el nivel de riesgo identificado (Bajo, Medio, Alto o Crítico) con su descripción, y emitir su voto. El sistema calcula el resultado: si más del 50% vota a favor, la solicitud avanza; de lo contrario es rechazada. |
| **Requisitos relacionados** | RF-26, RF-27, RF-28                                                                                                                                                                                                                                                                                                                                      |
| **Reglas de negocio**       | RN-06, RN-07, RN-08             

<img width="1440" height="2960" alt="image" src="https://github.com/user-attachments/assets/e46227f1-6a9d-449e-88c2-3cdfbf872a74" />
|
