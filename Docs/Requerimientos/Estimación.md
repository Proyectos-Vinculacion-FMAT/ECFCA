Clasificacin:

|  |  |  |  |
| --- | --- | --- | --- |
| Categora | Interacciones (Backend/Frontend) | Operaciones (CRUD) | Interfaces Requeridas |
| Sencillo | 1-2 interacciones directas | 1-2 operaciones (ej. solo C o solo R) | 1-2 interfaces |
| Mediano | 3-5 interacciones complejas | 3-5 operaciones (ej. C, R, U) | 3-4 interfaces |
| Complicado | 6+ interacciones o ms | 6+ operaciones o lgica avanzada | 5+ interfaces o mltiples estados |

**Resumen de Casos de Uso por Categora**

|  |  |  |
| --- | --- | --- |
| Sencillo: 25 casos de uso | Mediano: 15 casos de uso | Complicado: 2 casos de uso |
| CU-GE-002 Consultar Eventos CU-GE-004 Eliminar Evento CU-GE-009 Crear Categora de Evento/Capacitacin CU-GE-010 Consultar Categoras de Evento/Capacitacin CU-GE-011 Modificar Categora de Evento/Capacitacin CU-GE-012 Eliminar Categora de Evento/Capacitacin CU-MU-001 Consultar Usuarios CU-MU-003 Registrar Capacitador CU-MU-004 Consultar Capacitadores CU-MU-006 Archivar/Eliminar Capacitador CU-MU-008 Validar Informacin de Pago/Facturacin Propia CU-MU-009 Consultar Capacitaciones Asignadas CU-PG-003 Gestionar Datos Personales (Pblico General) CU-PG-006 Cargar Documentos (por el usuario) CU-PG-007 Consultar Estado de mis Solicitudes/Inscripciones CU-PG-009 Consultar Mis Eventos CU-VE-002 Agregar lead manualmente CU-VE-004 Asignar leads CU-VE-005 Convertir lead en oportunidad CU-VE-006 Registrar Interaccin con Oportunidad CU-VE-007 Agendar Tarea de Seguimiento CU-VE-008 Cerrar Oportunidad Ganada-Perdida CU-VE-009 Consultar recordatorios CU-VE-011 Cargar Documentacin en Nombre del Cliente CU-VE-012 Consultar estado del pago | CU-GE-001 Crear Evento CU-GE-003 Modificar Evento CU-GE-005 Generar Constancias CU-GE-006 Generar Reportes de Eventos CU-GE-007 Aprobar/Gestionar Solicitudes de Inscripcin CU-GE-008 Validar Pagos Manuales CU-MU-002 Validar documentacin CU-MU-005 Modificar Informacin de Capacitador CU-MU-007 Registrar/Actualizar Informacin de Pago/Facturacin de Capacitador CU-PG-001 Iniciar Sesin CU-PG-002 Crear Cuenta CU-PG-004 Solicitar Inscripcin a Evento CU-PG-008 Volver a Enviar Solicitud CU-VE-003 Visualizar leads CU-VE-010 Gestionar Notificacin de Recordatorio | CU-PG-005 Realizar Pago de Solicitud Aprobada CU-VE-001 Recuperar leads de fuentes externas |

**Mdulo: Gestin de Eventos**

**CU-GE-001 Crear Evento**

* **Categora:** **Mediano**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Se requieren mltiples interacciones. Primero, el frontend podra necesitar cargar listas de datos (ej. capacitadores disponibles) para poblar los campos del formulario. Luego, hay una interaccin para el envo de los datos principales del evento. Adicionalmente, puede haber interacciones asncronas para subir imgenes o documentos relacionados con el evento. Esto suma al menos 3 interacciones separadas.
  + **Operaciones (CRUD):** Este caso de uso va ms all de una simple operacin de creacin. Implica: 1) la operacin principal de **Crear** el registro del evento, y 2) la **Creacin** de registros relacionados (ej. las relaciones entre el evento y sus capacitadores o categoras).
  + **Interfaces Requeridas:** Generalmente, se necesita una interfaz compleja de tipo formulario, que podra incluir una segunda interfaz (un modal o pop-up) para seleccionar recursos o subir archivos.

**CU-GE-002 Consultar Eventos**

* **Categora:** **Sencillo**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Solo requiere una interaccin con el backend para solicitar y recibir la lista de eventos. No hay un flujo de datos complejo.
  + **Operaciones (CRUD):** Es una operacin de **Lectura** (Read) directa.
  + **Interfaces Requeridas:** Se necesitan dos interfaces: una para la lista de eventos y otra para la vista de detalles de un evento seleccionado. La navegacin entre ellas es lineal.

**CU-GE-003 Modificar Evento**

* **Categora:** **Mediano**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Se requieren al menos dos interacciones: 1) para cargar los datos existentes del evento en el formulario de edicin, y 2) para enviar los datos actualizados.
  + **Operaciones (CRUD):** Involucra una operacin de **Lectura** (Read) para obtener los datos actuales y una operacin de **Actualizacin** (Update) para guardar los cambios.
  + **Interfaces Requeridas:** Se necesita una interfaz de lista (para encontrar el evento a modificar) y una interfaz de formulario de edicin. Esto suma al menos 2 interfaces principales.

**CU-GE-004 Eliminar Evento**

* **Categora:** **Sencillo**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Una nica interaccin para enviar la solicitud de borrado al backend.
  + **Operaciones (CRUD):** Una operacin de **Borrado** (Delete) directa.
  + **Interfaces Requeridas:** Una interfaz (la lista de eventos) y un pop-up de confirmacin.

**CU-GE-005 Generar Constancias**

* **Categora:** **Mediano**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Puede ser una sola interaccin, pero desencadena un proceso complejo en el backend.
  + **Operaciones (CRUD):** No es una operacin CRUD estndar. Involucra una lgica de negocio avanzada que lee datos de usuarios, eventos y asistentes, y luego genera un nuevo tipo de archivo (un PDF).
  + **Interfaces Requeridas:** Una interfaz para la seleccin de parmetros de generacin y un mensaje de confirmacin de que el proceso ha iniciado.

**CU-GE-006 Generar Reportes de Eventos**

* **Categora:** **Mediano**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Similar a Generar Constancias. Requiere una interaccin para solicitar el reporte, pero el backend realiza mltiples operaciones de lectura para consolidar la informacin.
  + **Operaciones (CRUD):** Se basa principalmente en operaciones de **Lectura** (Read) de mltiples fuentes de datos, pero la complejidad de consolidar y transformar esos datos en un reporte lo clasifica como mediano.
  + **Interfaces Requeridas:** Se necesita una interfaz de filtros para que el usuario pueda especificar qu tipo de reporte necesita.

**CU-GE-007 Aprobar/Gestionar Solicitudes de Inscripcin**

* **Categora:** **Mediano**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Mltiples interacciones: 1) consultar la lista de solicitudes, 2) consultar los detalles de una solicitud, y 3) enviar la actualizacin del estado de la solicitud (aprobado/rechazado).
  + **Operaciones (CRUD):** Requiere operaciones de **Lectura** (Read) y **Actualizacin** (Update).
  + **Interfaces Requeridas:** Una interfaz de lista de solicitudes y un pop-up o vista de detalles para gestionar cada una.

**CU-GE-008 Validar Pagos Manuales**

* **Categora:** **Mediano**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Requiere mltiples interacciones para consultar los pagos pendientes, ver los detalles de un pago, y luego enviar la actualizacin del estado de validacin.
  + **Operaciones (CRUD):** Se utilizan operaciones de **Lectura** (Read) y **Actualizacin** (Update).
  + **Interfaces Requeridas:** Una interfaz de lista de pagos y un pop-up de confirmacin/formulario de validacin.

**CU-GE-009 Crear Categora de Evento/Capacitacin**

* **Categora:** **Sencillo**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Una nica interaccin para enviar los datos de la nueva categora.
  + **Operaciones (CRUD):** Una operacin de **Creacin** (Create).
  + **Interfaces Requeridas:** Una interfaz de formulario bsica.

**CU-GE-010 Consultar Categoras de Evento/Capacitacin**

* **Categora:** **Sencillo**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Una sola interaccin para obtener la lista de categoras.
  + **Operaciones (CRUD):** Una operacin de **Lectura** (Read).
  + **Interfaces Requeridas:** Una interfaz de lista.

**CU-GE-011 Modificar Categora de Evento/Capacitacin**

* **Categora:** **Sencillo**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Dos interacciones: una para obtener los datos de la categora y otra para enviar la actualizacin.
  + **Operaciones (CRUD):** Una operacin de **Lectura** (Read) y una de **Actualizacin** (Update).
  + **Interfaces Requeridas:** Una interfaz de lista y un formulario de edicin.

**CU-GE-012 Eliminar Categora de Evento/Capacitacin**

* **Categora:** **Sencillo**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Una nica interaccin para la solicitud de borrado.
  + **Operaciones (CRUD):** Una operacin de **Borrado** (Delete).
  + **Interfaces Requeridas:** Una interfaz de lista y un pop-up de confirmacin.

**Mdulo: Gestin de Usuarios**

**CU-MU-001 Consultar Usuarios**

* **Categora:** **Sencillo**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Una interaccin para obtener la lista de usuarios.
  + **Operaciones (CRUD):** Una operacin de **Lectura** (Read).
  + **Interfaces Requeridas:** Una interfaz de lista y una de detalles.

**CU-MU-002 Validar documentacin**

* **Categora:** **Mediano**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Varias interacciones: 1) cargar la lista de usuarios con documentacin pendiente, 2) obtener los documentos especficos de un usuario, y 3) enviar el estado de validacin.
  + **Operaciones (CRUD):** Una operacin de **Lectura** (Read) y una de **Actualizacin** (Update).
  + **Interfaces Requeridas:** Una interfaz de lista de usuarios, una interfaz de visualizacin de documentos y un pop-up de validacin.

**CU-MU-003 Registrar Capacitador**

* **Categora:** **Sencillo**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Una interaccin para enviar el formulario de registro.
  + **Operaciones (CRUD):** Una operacin de **Creacin** (Create).
  + **Interfaces Requeridas:** Un nico formulario.

**CU-MU-004 Consultar Capacitadores**

* **Categora:** **Sencillo**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Una interaccin para obtener la lista de capacitadores.
  + **Operaciones (CRUD):** Una operacin de **Lectura** (Read).
  + **Interfaces Requeridas:** Una interfaz de lista y una de detalles.

**CU-MU-005 Modificar Informacin de Capacitador**

* **Categora:** **Mediano**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Dos interacciones: una para obtener los datos del capacitador y otra para enviar la actualizacin.
  + **Operaciones (CRUD):** Una operacin de **Lectura** (Read) y una de **Actualizacin** (Update).
  + **Interfaces Requeridas:** Una interfaz de lista, una de detalle y un formulario de edicin.

**CU-MU-006 Archivar/Eliminar Capacitador**

* **Categora:** **Sencillo**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Una interaccin para enviar la solicitud de cambio de estado.
  + **Operaciones (CRUD):** Una operacin de **Borrado** (Delete) o **Actualizacin** (Update) de estado.
  + **Interfaces Requeridas:** Una interfaz de lista con un pop-up de confirmacin.

**CU-MU-007 Registrar/Actualizar Informacin de Pago/Facturacin de Capacitador**

* **Categora:** **Mediano**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Varias interacciones: obtener la informacin existente, enviar los datos actualizados y posiblemente validar la informacin.
  + **Operaciones (CRUD):** Puede ser una **Creacin** (Create) o una **Actualizacin** (Update), dependiendo de si los datos existen o no. La naturaleza sensible de la informacin agrega complejidad.
  + **Interfaces Requeridas:** Un formulario dedicado a los datos de pago y facturacin.

**CU-MU-008 Validar Informacin de Pago/Facturacin Propia**

* **Categora:** **Sencillo**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Una nica interaccin para obtener los datos del usuario.
  + **Operaciones (CRUD):** Una operacin de **Lectura** (Read).
  + **Interfaces Requeridas:** Una sola interfaz para visualizar la informacin.

**CU-MU-009 Consultar Capacitaciones Asignadas**

* **Categora:** **Sencillo**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Una interaccin para obtener la lista de capacitaciones.
  + **Operaciones (CRUD):** Una operacin de **Lectura** (Read).
  + **Interfaces Requeridas:** Una interfaz de lista.

**Mdulo: Pblico General**

**CU-PG-001 Iniciar Sesin**

* **Categora:** **Mediano**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Mltiples interacciones: 1) enviar el correo, 2) recibir el correo, 3) enviar el cdigo para su validacin, 4) verificar el estado del usuario.
  + **Operaciones (CRUD):** El proceso no es un CRUD tpico, pero involucra la **Creacin** de un token temporal y su posterior **Actualizacin** de estado.
  + **Interfaces Requeridas:** Al menos 3 interfaces: una pantalla para ingresar el correo, una pantalla para ingresar el cdigo y una pantalla de confirmacin.

**CU-PG-002 Crear Cuenta**

* **Categora:** **Mediano**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Similar a Iniciar Sesin. Requiere mltiples interacciones para registrar los datos iniciales, enviar el correo de verificacin y validar el cdigo.
  + **Operaciones (CRUD):** Se crea un registro de usuario, se crea un token temporal y se actualiza el estado de la cuenta.
  + **Interfaces Requeridas:** Un formulario de registro, una pantalla de verificacin de correo y una pantalla de confirmacin.

**CU-PG-003 Gestionar Datos Personales (Pblico General)**

* **Categora:** **Sencillo**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Dos interacciones: una para obtener los datos existentes y otra para enviar la actualizacin.
  + **Operaciones (CRUD):** Una operacin de **Lectura** (Read) y una de **Actualizacin** (Update).
  + **Interfaces Requeridas:** Una interfaz para ver el perfil y un formulario para editarlo.

**CU-PG-004 Solicitar Inscripcin a Evento**

* **Categora:** **Mediano**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Mltiples interacciones. Se necesita enviar los datos del formulario de inscripcin y, de forma incluida, se activan las interacciones para **Cargar Documentos**.
  + **Operaciones (CRUD):** Una operacin de **Creacin** (Create) para el registro de la solicitud.
  + **Interfaces Requeridas:** Un formulario de solicitud, la interfaz para la carga de documentos y una de confirmacin.

**CU-PG-005 Realizar Pago de Solicitud Aprobada**

* **Categora:** **Complicado**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Mltiples interacciones. El frontend se comunica con el backend, y el backend interacta con un **servicio de terceros** (la pasarela de pagos). Esto genera mltiples flujos de datos.
  + **Operaciones (CRUD):** Implica una **Actualizacin** (Update) del estado de la solicitud de "aprobada" a "pagada" y la **Creacin** de un registro de transaccin.
  + **Interfaces Requeridas:** Una interfaz para iniciar el pago, y luego la interfaz de la pasarela de pagos. Los mensajes de xito o fracaso tambin cuentan.

**CU-PG-006 Cargar Documentos (por el usuario)**

* **Categora:** **Sencillo**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Una sola interaccin para enviar el archivo al servidor.
  + **Operaciones (CRUD):** Una operacin de **Creacin** (Create) de un registro de documento.
  + **Interfaces Requeridas:** Un campo de subida de archivos y un mensaje de confirmacin.

**CU-PG-007 Consultar Estado de mis Solicitudes/Inscripciones**

* **Categora:** **Sencillo**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Una interaccin para obtener la lista de solicitudes del usuario.
  + **Operaciones (CRUD):** Una operacin de **Lectura** (Read) directa.
  + **Interfaces Requeridas:** Una interfaz de lista y una de detalles.

**CU-PG-008 Volver a Enviar Solicitud**

* **Categora:** **Mediano**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Mltiples interacciones: 1) cargar la solicitud rechazada, 2) permitir la edicin, 3) enviar los datos corregidos.
  + **Operaciones (CRUD):** Involucra **Lectura** (Read) de la solicitud original y **Actualizacin** (Update) de la misma.
  + **Interfaces Requeridas:** Una interfaz para ver la solicitud rechazada y un formulario de edicin que puede incluir la interfaz de carga de documentos.

**CU-PG-009 Consultar Mis Eventos**

* **Categora:** **Sencillo**
* **Justificacin Detallada:**
  + **Interacciones (Backend/Frontend):** Una interaccin para obtener la lista de eventos inscritos.
  + **Operaciones (CRUD):** Una operacin de **Lectura** (Read) directa.
  + **Interfaces Requeridas:** Una interfaz de lista y, opcionalmente, una de detalles.

**Módulo: Ventas**

**CU-VE-001 Recuperar leads de fuentes externas**

* **Categoría:** **Complicado**
* **Justificación Detallada:**
    * **Interacciones (Backend/Frontend):** Múltiples interacciones con APIs externas (Meta, UADY), manejo de webhooks o tareas programadas. Lógica de negocio compleja para la normalización y el mapeo de datos.
    * **Operaciones (CRUD):** Implica operaciones de **Creación** (nuevos leads) y **Actualización** (leads duplicados que se enriquecen). La lógica de detección de duplicados añade complejidad.
    * **Interfaces Requeridas:** Aunque es un proceso de backend, requiere interfaces de configuración para las APIs, mapeo de campos y visualización de logs de importación.

**CU-VE-002 Agregar lead manualmente**

* **Categoría:** **Sencillo**
* **Justificación Detallada:**
    * **Interacciones (Backend/Frontend):** Una única interacción para enviar el formulario.
    * **Operaciones (CRUD):** Una operación de **Creación** (Create).
    * **Interfaces Requeridas:** Una interfaz de formulario.

**CU-VE-003 Visualizar leads**

* **Categoría:** **Mediano**
* **Justificación Detallada:**
    * **Interacciones (Backend/Frontend):** Múltiples interacciones para aplicar filtros y paginación.
    * **Operaciones (CRUD):** Operación de **Lectura** (Read) con lógica de negocio para filtrar por múltiples criterios y roles.
    * **Interfaces Requeridas:** Una interfaz de lista con controles de filtrado complejos y paginación. La vista varía según el rol (Agente vs. Jefe de Área).

**CU-VE-004 Asignar leads**

* **Categoría:** **Sencillo**
* **Justificación Detallada:**
    * **Interacciones (Backend/Frontend):** Pocas interacciones: seleccionar leads, seleccionar agente, confirmar.
    * **Operaciones (CRUD):** Una operación de **Actualización** (Update) en uno o varios registros.
    * **Interfaces Requeridas:** Una interfaz de lista y un modal o pop-up de asignación.

**CU-VE-005 Convertir lead en oportunidad**

* **Categoría:** **Sencillo**
* **Justificación Detallada:**
    * **Interacciones (Backend/Frontend):** Una interacción principal para la conversión.
    * **Operaciones (CRUD):** Implica una **Actualización** (Update) del estado del lead y la **Creación** (Create) de un nuevo registro de oportunidad.
    * **Interfaces Requeridas:** Un botón en la ficha del lead y un modal de confirmación.

**CU-VE-006 Registrar Interacción con Oportunidad**

* **Categoría:** **Sencillo**
* **Justificación Detallada:**
    * **Interacciones (Backend/Frontend):** Una interacción para guardar la nota o el estado.
    * **Operaciones (CRUD):** Una operación de **Creación** (Create) de un registro de interacción en la bitácora.
    * **Interfaces Requeridas:** Un formulario simple o menú dentro de la ficha de la oportunidad.

**CU-VE-007 Agendar Tarea de Seguimiento**

* **Categoría:** **Sencillo**
* **Justificación Detallada:**
    * **Interacciones (Backend/Frontend):** Una interacción para guardar la tarea.
    * **Operaciones (CRUD):** Una operación de **Creación** (Create).
    * **Interfaces Requeridas:** Un formulario para agendar la tarea.

**CU-VE-008 Cerrar Oportunidad Ganada-Perdida**

* **Categoría:** **Sencillo**
* **Justificación Detallada:**
    * **Interacciones (Backend/Frontend):** Una interacción para cerrar la oportunidad.
    * **Operaciones (CRUD):** Una operación de **Actualización** (Update) del estado de la oportunidad.
    * **Interfaces Requeridas:** Un modal o formulario para seleccionar el estado final y el motivo.

**CU-VE-009 Consultar recordatorios**

* **Categoría:** **Sencillo**
* **Justificación Detallada:**
    * **Interacciones (Backend/Frontend):** Una interacción para obtener la lista de recordatorios.
    * **Operaciones (CRUD):** Una operación de **Lectura** (Read).
    * **Interfaces Requeridas:** Una interfaz de lista.

**CU-VE-010 Gestionar Notificación de Recordatorio**

* **Categoría:** **Mediano**
* **Justificación Detallada:**
    * **Interacciones (Backend/Frontend):** Múltiples interacciones: recibir la notificación, y luego completarla, posponerla o descartarla.
    * **Operaciones (CRUD):** Implica la **Actualización** (Update) del estado de la tarea/recordatorio.
    * **Interfaces Requeridas:** Componentes de notificación y modales para gestionar la tarea.

**CU-VE-011 Cargar Documentación en Nombre del Cliente**

* **Categoría:** **Sencillo**
* **Justificación Detallada:**
    * **Interacciones (Backend/Frontend):** Una interacción para subir el archivo.
    * **Operaciones (CRUD):** Una operación de **Creación** (Create) de un registro de documento.
    * **Interfaces Requeridas:** Un campo de subida de archivos.

**CU-VE-012 Consultar estado del pago**

* **Categoría:** **Sencillo**
* **Justificación Detallada:**
    * **Interacciones (Backend/Frontend):** Una interacción para obtener el estado.
    * **Operaciones (CRUD):** Una operación de **Lectura** (Read).
    * **Interfaces Requeridas:** Un campo informativo en la ficha de la oportunidad.