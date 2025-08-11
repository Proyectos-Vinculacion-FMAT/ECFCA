# Proyecto FCA-Educación Continua

> Este proyecto se encuentra actualmente en la fase de requerimientos, cualquier información presentada está sujeta a cambios en el futuro.

| <image src="assets/fca-ec_logo.png"  height="100"/> | <image height="100" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRuDMIMdlxdcdxQFfb0kD1qVYzOJ3GvoIMVgg&s"/> |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |

Proyecto En colaboración entre los departamentos de **Vinculación** de la **Facultad de Matemáticas** y de **Contaduría y Administración**.

<center>

**Responsable**

Edgar Antonio Cambranes Martínez

**Elaborado por**

Rodrigo Joaquín Pacab Canul <br>
Carlos Roberto Ek Raigoza
</center>

## Resumen

Sistema integral de gestión académica y comercial diseñado para automatizar y optimizar la administración de eventos educativos, desde la captación de leads hasta la emisión de constancias.

La plataforma centraliza la gestión de capacitaciones, cursos y diplomados a través de tres módulos principales:

- Gestión de Eventos para la creación y administración de programas académicos,
- Gestión de Usuarios para el manejo de capacitadores y participantes,
- y Gestión de Ventas que automatiza la captación de leads desde fuentes externas como Meta Ads y la bolsa de trabajo de la UADY, convirtiendo prospectos en oportunidades de venta mediante un embudo comercial estructurado.

El sistema facilita todo el ciclo de vida del público general, desde su registro inicial como interesado, pasando por el proceso de solicitud e inscripción con validación de documentos y pagos, hasta su participación activa con acceso a sus eventos inscritos y la generación automática de constancias de participación, proporcionando una solución completa que integra los aspectos académicos y comerciales de la institución educativa.

> **Importante:** En este punto del proyecto aún no se cuenta con información relevante proveniente del departamento de Contabilidad, sin embargo se considera su interacción en el proceso de gestión de pagos y facturación.

## Recopilación de Requerimientos

La siguiente imagen presenta de manera informal el flujo de información y las acciones del departamento, identificando los puntos críticos donde se manifiestan las problemáticas actuales. Estas dificultades tienen su origen en deficiencias estructurales del proceso completo, a pesar de ser posiblemente las que más se sienten en puntos particulares del proceso.

<details>
<summary>
Ver imagen
</summary>

![Bosquejo del problema](docs/Análisis/Problema/Bosquejo%20del%20problema.png)

</details>

### Alcance

![alt](Docs/Análisis/Problema/Diagrama%20de%20Contexto.png)

El alcance del sistema incluye la gestión de eventos, usuarios y ventas, abarcando desde la captación de leads hasta la emisión de constancias de participación. Si  bien los problemas con contabilidad son el síntoma más palpable, es una consecuencia de la estructura y falta de control preciso del proceso entero.

### Identificación de interesados


![diagrama de cebolla](Docs/Análisis/Problema/Diagrama%20de%20cebolla-stakeholders.png)

> Diagrama de cebolla para ilustrar el nivel de prioridad e interacción de los interesados en el sistema.

## Elaboración de Casos de Uso

Los casos de uso son una forma de representar los requisitos funcionales del sistema desde la perspectiva del usuario. Cada caso de uso describe una interacción específica entre un actor y el sistema, detallando los pasos necesarios para lograr un objetivo particular.

### Actores del sistema

![alt](Docs/Requerimientos/Diagramas/img/System%20Actors.png)

**Actores identificados:**
- Usuario
- Staff
- Coordinación
- Capacitador
- Público General
- Personal de Contabilidad
- Promotor de Ventas
- Responsable de Ventas
- Coordinadora de EC
- Coordinadora de Vinculación
- Equipo de Ventas
- Interesado (lead/opportunity)
- Participante
- Meta Ads

### Sistema completo: Vista global

![alt](Docs/Requerimientos/Diagramas/img/Use%20Case%20System.png)

*El diagrama del sistema completo incluye todos los módulos y casos de uso del sistema integrado.*

### Acceso y Perfiles

![alt](Docs/Requerimientos/Diagramas/img/Acceso%20y%20Perfiles.png)

**Casos de uso relacionados:**
- **CU-PG-001**: Iniciar Sesión
- **CU-PG-002**: Crear Cuenta
- **CU-PG-003**: Gestionar Datos Personales

### Gestión de Eventos

![alt](Docs/Requerimientos/Diagramas/img/Gestión%20de%20Eventos.png)

**Casos de uso relacionados:**
- **CU-GE-001**: Crear Evento
- **CU-GE-002**: Consultar Eventos
- **CU-GE-003**: Modificar Evento
- **CU-GE-004**: Eliminar Evento
- **CU-GE-005**: Generar Constancias
- **CU-GE-006**: Generar Reportes de Eventos
- **CU-GE-007**: Aprobar-Gestionar Solicitudes de Inscripción
- **CU-GE-008**: Validar Pagos Manuales
- **CU-GE-009**: Crear Categoría de Evento-Capacitación
- **CU-GE-010**: Consultar Categorías de Evento-Capacitación
- **CU-GE-011**: Modificar Categoría de Evento-Capacitación
- **CU-GE-012**: Eliminar Categoría de Evento-Capacitación

### Gestión de leads

![alt](Docs/Requerimientos/Diagramas/img/Gestión%20de%20leads.png)

**Casos de uso relacionados:**
- **CU-VE-001**: Recuperar leads de fuentes externas
- **CU-VE-002**: Agregar lead manualmente
- **CU-VE-003**: Visualizar leads
- **CU-VE-004**: Asignar leads
- **CU-VE-005**: Convertir lead en oportunidad

### Gestión de oportunidades

![alt](Docs/Requerimientos/Diagramas/img/Gestión%20de%20oportunidades.png)

**Casos de uso relacionados:**
- **CU-VE-006**: Registrar Interacción con Oportunidad
- **CU-VE-007**: Agendar Tarea de Seguimiento
- **CU-VE-008**: Cerrar Oportunidad Ganada-Perdida
- **CU-VE-009**: Consultar recordatorios
- **CU-VE-010**: Gestionar Notificación de Recordatorio
- **CU-VE-011**: Cargar Documentación en Nombre del Cliente
- **CU-VE-012**: Consultar estado del pago

### Usuarios

![alt](Docs/Requerimientos/Diagramas/img/Módulo%20de%20Usuarios.png)

**Casos de uso relacionados:**
- **CU-MU-001**: Consultar Usuarios
- **CU-MU-002**: Validar documentación
- **CU-MU-003**: Registrar Capacitador
- **CU-MU-004**: Consultar Capacitadores
- **CU-MU-005**: Modificar Información de Capacitador
- **CU-MU-006**: Archivar-Eliminar Capacitador
- **CU-MU-007**: Registrar-Actualizar Información de Pago-Facturación de Capacitador
- **CU-MU-008**: Validar Información de Pago-Facturación Propia
- **CU-MU-009**: Consultar Capacitaciones Asignadas

### Público General

![alt](Docs/Requerimientos/Diagramas/img/Público%20General.png)

**Casos de uso relacionados:**
- **CU-PG-004**: Solicitar Inscripción a Evento
- **CU-PG-005**: Realizar Pago de Solicitud Aprobada
- **CU-PG-006**: Cargar Documentos (por el usuario)
- **CU-PG-007**: Consultar Estado de mis Solicitudes-Inscripciones
- **CU-PG-008**: Volver a Enviar Solicitud
- **CU-PG-009**: Consultar Mis Eventos



## Estimación de Requerimientos

Disponible en [Estimación](Docs/Requerimientos/Estimación.md)
