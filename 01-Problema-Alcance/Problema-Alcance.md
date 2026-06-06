# Problema y alcance

Nexa Servicios enfrenta un problema sistémico de desorden digital que compromete la gobernanza de sus procesos operativos y tecnológicos. En la práctica diaria, las solicitudes se originan en canales no estructurados —mensajes de WhatsApp en grupos incorrectos, correos con múltiples copias y archivos Excel con nombres de versiones ambiguas— y, con el crecimiento organizacional, estas prácticas han provocado la dispersión de la información, la pérdida de evidencias y la incapacidad para reconstruir el ciclo de vida de un cambio.

Estudios recientes sobre el uso de mensajería instantánea en la empresa muestran que, aunque herramientas como WhatsApp aceleran la comunicación y aumentan la colaboración, también introducen riesgos de confidencialidad, fragmentación de la información y dificultad para auditar decisiones cuando no se integran a flujos formales de trabajo.

## Falta de control y trazabilidad

Desde la perspectiva de control y cumplimiento, la ausencia de un repositorio centralizado y de políticas de versionado implica que no exista una traza verificable de quién solicitó, aprobó o implementó un cambio.

La literatura sobre gobernanza de datos y trazabilidad destaca que los entornos heterogéneos sin estándares de registro complican la reconstrucción de historiales y el cumplimiento regulatorio, especialmente en organizaciones con múltiples sistemas y comunicaciones fragmentadas. Implementar prácticas de gobernanza y registro es una condición previa para garantizar la auditabilidad y la rendición de cuentas.

## Necesidad de un proceso formal de control de cambios

En términos operativos, la solución técnica más adecuada para corregir este desorden pasa por formalizar un proceso de **control de cambios (Change Control)** que incluya:

- Definición de estados de la solicitud:
  - Registrada
  - Evaluada
  - Aprobada
  - Implementada
  - Verificada
  - Cerrada

- Roles claramente asignados:
  - Solicitante
  - Evaluador
  - Aprobador
  - Responsable de implementación

- Un registro inmutable o con control de versiones que almacene evidencias de aprobación y ejecución.

Marcos y guías contemporáneas de gestión de cambios, como los principios de **ITIL 4** y las prácticas de **IT Service Management (ITSM)**, recomiendan este tipo de controles para minimizar riesgos operativos y asegurar la continuidad del servicio.

## Implementación de una plataforma centralizada

La adopción de un sistema de ticketing o plataforma de gestión de solicitudes centralizada, integrada idealmente con registro de evidencias y control de versiones de documentos, ha demostrado reducir tiempos de resolución, eliminar duplicidades y proporcionar paneles de seguimiento que facilitan la priorización y la asignación de recursos.

La evidencia empírica en entornos de TI señala mejoras significativas en trazabilidad y en la capacidad de auditoría cuando las solicitudes dejan de circular por canales informales y se registran en un sistema único.

## Control documental y versionado

Las buenas prácticas en control documental y versionado constituyen requisitos fundamentales para mantener la integridad de la información y facilitar auditorías internas y externas. Entre estas prácticas se incluyen:

- Convenciones estandarizadas de nombres (*naming conventions*).
- Almacenamiento centralizado de documentos.
- Flujos formales de aprobación.
- Bitácoras automáticas de cambios.

Asimismo, la automatización parcial del registro de evidencias mediante mecanismos como:

- Firmas digitales.
- Metadatos de versiones.
- Bitácoras auditables generadas por la plataforma.

permite reducir la dependencia del factor humano y aumentar la confianza en la trazabilidad de los cambios realizados.

## Alcance de la propuesta

La propuesta contempla el diseño e implementación de un sistema centralizado de gestión y control de cambios que permita:

1. Registrar formalmente todas las solicitudes operativas y tecnológicas.
2. Mantener evidencia verificable de cada aprobación y ejecución.
3. Establecer un flujo de trabajo estandarizado para la gestión de cambios.
4. Mejorar la trazabilidad y auditabilidad de los procesos.
5. Reducir la dependencia de canales informales de comunicación.
6. Fortalecer la gobernanza tecnológica y el control documental dentro de Nexa Servicios.

## Referencias seleccionadas (últimos 5 años)

1. Tarofder, A. K., et al. (2024). *Instant Messaging: Benchmarking Its Impact in the Workplace*. ScienceDirect.
2. De (A.), et al. (2025). *Business on WhatsApp is Tough Now — But Am I Really a...*. ACM Digital Library.
3. Bernardo, B. M. V. (2024). *Data Governance & Quality Management—Innovation and Practice*. ScienceDirect.
4. *Compliance, Traceability, and Auditability in Mixed ISO 8583 / ISO 20022 Environments* (2026). ResearchGate.
5. PDC A Consulting (2025). *Comprehensive Guide to ITIL 4 Change Management*.
6. Effivity / Legal Document Simplifier (2025). *Best Practices for Document Version Control and Quality Management Systems (QMS)*.
7. Estudios empíricos sobre sistemas de ticketing y gestión de solicitudes que evidencian mejoras en trazabilidad, tiempos de respuesta y capacidad de auditoría en entornos de TI.
