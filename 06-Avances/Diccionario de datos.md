# 4. Diccionario de Datos

El diccionario de datos define todas las entidades, atributos y datos relevantes identificados en el documento de requisitos aprobado. Se organiza por módulo o entidad. Los tipos de datos, longitudes y restricciones se infieren a partir de los requisitos funcionales y reglas de negocio documentados; donde no existe especificación explícita, se indica la inferencia realizada.

## 4.1 Entidad: Solicitud de Cambio

Representa el registro central del sistema. Cada solicitud agrupa toda la información del cambio solicitado, su ciclo de vida y su evidencia asociada.

| Atributo                    | Descripción                                                            | Tipo          | Formato / Longitud                        | Restricciones                                                | Ejemplo                                                                      |
| --------------------------- | ---------------------------------------------------------------------- | ------------- | ----------------------------------------- | ------------------------------------------------------------ | ---------------------------------------------------------------------------- |
| Radicado                    | Identificador único y automático de la solicitud.                      | Texto         | CAM-AAAA-NNN (12 car.)                    | No nulo. Único. Generado por el sistema. No editable.        | CAM-2025-001                                                                 |
| Título                      | Nombre corto y descriptivo del cambio solicitado.                      | Texto         | Máx. 150 caracteres                       | No nulo. Obligatorio al registrar.                           | Actualización de servidor de base de datos                                   |
| Descripción                 | Explicación detallada del cambio que se solicita.                      | Texto largo   | Sin límite definido                       | No nulo. Obligatorio al registrar.                           | Se requiere actualizar el motor de base de datos de la versión 5.7 a la 8.0. |
| Justificación               | Razón por la cual se solicita el cambio. Exigida por RN-01.            | Texto largo   | Sin límite definido                       | No nulo. Obligatorio antes de enviar. (RN-01)                | La versión actual no recibe soporte de seguridad desde enero de 2025.        |
| Área afectada               | Departamento o área de la empresa que se verá impactada.               | Texto / Lista | Valores predefinidos por el administrador | No nulo. Selección de lista configurada (RF-24).             | Tecnología de Información                                                    |
| Fecha esperada              | Fecha en que se planea implementar el cambio.                          | Fecha         | AAAA-MM-DD                                | No nulo. Debe ser una fecha presente o futura.               | 2025-09-15                                                                   |
| Estado                      | Estado actual de la solicitud dentro del flujo del proceso.            | Enumerado     | Ver estados definidos                     | No nulo. Controlado por el sistema. No editable manualmente. | Aprobada                                                                     |
| Nivel de riesgo             | Clasificación del riesgo asociado al cambio. Registrado por el comité. | Enumerado     | Bajo / Medio / Alto / Crítico             | Obligatorio para cambios de alto impacto (RN-06).            | Alto                                                                         |
| Fecha de creación           | Fecha y hora en que la solicitud fue registrada en el sistema.         | Fecha y hora  | AAAA-MM-DD HH:MM:SS                       | Generada automáticamente por el sistema. No editable.        | 2025-08-20 10:35:22                                                          |
| Resultado de implementación | Resultado registrado por el técnico al ejecutar el cambio.             | Enumerado     | Exitosa / Parcial / Fallida               | Obligatorio al registrar la implementación (RF-12).          | Exitosa                                                                      |

## 4.2 Entidad: Estados de la Solicitud (Flujo)

Define los valores permitidos para el atributo **Estado** de la solicitud y las condiciones de cada uno.

| Estado                   | Descripción                                  | Condición de entrada                                      | Ejemplo de situación                  |
| ------------------------ | -------------------------------------------- | --------------------------------------------------------- | ------------------------------------- |
| Pendiente de revisión    | Estado inicial al enviar la solicitud.       | El aprobador no ha revisado la solicitud aún.             | Solicitud recién enviada              |
| En revisión              | El aprobador está evaluando la solicitud.    | El aprobador abrió la solicitud para analizarla.          | Solicitud abierta por aprobador       |
| Pendiente de información | El aprobador requiere datos adicionales.     | El aprobador cambió el estado y notificó al solicitante.  | Aprobador solicita más datos          |
| En revisión por comité   | Solicitud de alto impacto enviada al comité. | El aprobador clasificó la solicitud como de alto impacto. | Cambio crítico en proceso de votación |
| Aprobada                 | La solicitud fue formalmente aprobada.       | El aprobador o comité aprobaron la solicitud.             | Lista para implementar                |
| Rechazada                | La solicitud fue formalmente rechazada.      | El aprobador o comité rechazaron la solicitud.            | Solicitud sin viabilidad              |
| En revisión técnica      | Implementación parcial en revisión.          | El técnico registró resultado Parcial.                    | Cambio incompleto en análisis         |
| Implementada             | El cambio fue ejecutado exitosamente.        | El técnico registró resultado Exitosa.                    | Cambio aplicado con éxito             |
| Revertida                | El cambio fue deshecho tras un fallo.        | El técnico ejecutó y registró la reversa.                 | Cambio revertido con evidencia        |
| Cerrada                  | Ciclo de vida de la solicitud finalizado.    | El supervisor cerró formalmente la solicitud.             | Proceso concluido                     |

## 4.3 Entidad: Archivo Adjunto

Representa los archivos de soporte vinculados a una solicitud de cambio.

| Atributo               | Descripción                                             | Tipo                   | Formato / Long.           | Restricciones                           | Ejemplo                                                     |
| ---------------------- | ------------------------------------------------------- | ---------------------- | ------------------------- | --------------------------------------- | ----------------------------------------------------------- |
| ID de archivo          | Identificador único del archivo en el sistema.          | Entero autoincremental | —                         | No nulo. Generado por el sistema.       | 1024                                                        |
| Radicado asociado      | Radicado de la solicitud a la que pertenece el archivo. | Texto                  | CAM-AAAA-NNN              | No nulo. Llave foránea hacia Solicitud. | CAM-2025-001                                                |
| Nombre del archivo     | Nombre original del archivo al momento de la carga.     | Texto                  | Máx. 255 caracteres       | No nulo.                                | evidencia_pruebas.pdf                                       |
| Formato                | Extensión del archivo cargado.                          | Enumerado              | PDF, JPG, PNG, DOCX, XLSX | Solo se aceptan estos formatos.         | PDF                                                         |
| Tamaño                 | Tamaño del archivo en megabytes.                        | Decimal                | —                         | Máximo 10 MB por archivo.               | 2.4 MB                                                      |
| Fecha de carga         | Fecha y hora en que el archivo fue adjuntado.           | Fecha y hora           | AAAA-MM-DD HH:MM:SS       | Generada automáticamente.               | 2025-08-20 10:40:15                                         |
| Cargado por            | Usuario que adjuntó el archivo.                         | Texto (correo)         | —                         | No nulo.                                | [jperez@nexaservicios.com](mailto:jperez@nexaservicios.com) |
| Cantidad por solicitud | Número máximo de archivos por solicitud.                | Entero                 | —                         | Mínimo 1, máximo 5 por solicitud.       | 3                                                           |

## 4.4 Entidad: Usuario

Representa a cualquier persona que tiene acceso al sistema.

| Atributo                    | Descripción                                    | Tipo                   | Formato / Long.                                                               | Restricciones                     | Ejemplo                                                     |
| --------------------------- | ---------------------------------------------- | ---------------------- | ----------------------------------------------------------------------------- | --------------------------------- | ----------------------------------------------------------- |
| ID de usuario               | Identificador único del usuario en el sistema. | Entero autoincremental | —                                                                             | No nulo. Generado por el sistema. | 105                                                         |
| Nombre completo             | Nombre y apellido del usuario.                 | Texto                  | Máx. 150 caracteres                                                           | No nulo.                          | Juan Pérez Gómez                                            |
| Correo institucional        | Correo electrónico de la organización.         | Texto (email)          | Máx. 100 caracteres                                                           | No nulo. Único.                   | [jperez@nexaservicios.com](mailto:jperez@nexaservicios.com) |
| Contraseña                  | Credencial de acceso del usuario.              | Texto cifrado          | —                                                                             | No nulo. Cifrada con bcrypt.      | [hash bcrypt]                                               |
| Área                        | Departamento al que pertenece el usuario.      | Texto / Lista          | Valores predefinidos                                                          | No nulo.                          | Tecnología de Información                                   |
| Rol                         | Función del usuario en el sistema.             | Enumerado              | Solicitante / Aprobador / Técnico de TI / Supervisor / Administrador / Comité | No nulo.                          | Aprobador                                                   |
| Estado de cuenta            | Indica si el usuario puede acceder al sistema. | Booleano               | Activo / Inactivo                                                             | No nulo.                          | Activo                                                      |
| Fecha de creación           | Fecha en que la cuenta fue creada.             | Fecha                  | AAAA-MM-DD                                                                    | Generada automáticamente.         | 2024-03-10                                                  |
| Intentos fallidos de acceso | Contador de intentos fallidos.                 | Entero                 | 0 a 5                                                                         | Bloqueo al llegar a 5.            | 0                                                           |
| Fecha de bloqueo            | Fecha y hora de bloqueo.                       | Fecha y hora           | AAAA-MM-DD HH:MM:SS                                                           | Nulo si no está bloqueada.        | 2025-08-21 14:22:10                                         |

> Continúa con las entidades:
>
> * **4.5 Decisión de Aprobación**
> * **4.6 Resultado de Implementación**
> * **4.7 Voto del Comité**
> * **4.8 Línea de Tiempo (Evento de Auditoría)**
> * **4.9 Notificación**
> * **4.10 Configuración del Sistema**
>
> siguiendo exactamente el mismo formato de tablas mostrado anteriormente.
