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

> **📋 Navegación rápida:**
> - [Actores del sistema](#actores-del-sistema)
> - [Sistema completo: Vista global](#sistema-completo-vista-global)
> - [Módulos principales](#módulos-principales):
>   - [Acceso y Perfiles](#acceso-y-perfiles)
>   - [Gestión de Eventos](#gestión-de-eventos)
>   - [Gestión de Usuarios](#usuarios)
>   - [Gestión de Ventas (CRM)](#módulo-de-ventas-crm)
>   - [Funcionalidades del Público General](#público-general)

### Actores del sistema

![alt](Docs/Requerimientos/Diagramas/img/System%20Actors.png)

**Actores identificados:**
- **Usuario**: Rol base del sistema
- **Staff**: Personal administrativo general
- **Coordinación**: Personal de coordinación académica
- **Capacitador**: Instructores y facilitadores
- **Público General**: Usuarios finales/participantes
- **Personal de Contabilidad**: Gestión financiera
- **Equipo de Ventas**: Promotor, Responsable de Ventas
- **Coordinadoras**: Educación Continua y Vinculación
- **Interesado**: Leads y oportunidades
- **Participante**: Usuarios inscritos en eventos
- **Meta Ads**: Integración externa para captación

### Sistema completo: Vista global

![alt](Docs/Requerimientos/Diagramas/img/Use%20Case%20System.png)

*El diagrama del sistema completo incluye todos los módulos y casos de uso del sistema integrado, mostrando la interacción entre los diferentes actores y las funcionalidades principales.*

---

## Módulos principales

### Acceso y Perfiles

![alt](Docs/Requerimientos/Diagramas/img/Acceso%20y%20Perfiles.png)

**Casos de uso relacionados:**
- **[CU-PG-001](Docs/Requerimientos/Casos%20de%20Uso/CU-PG-001%20Iniciar%20Sesión.md)**: Iniciar Sesión
- **[CU-PG-002](Docs/Requerimientos/Casos%20de%20Uso/CU-PG-002%20Crear%20Cuenta.md)**: Crear Cuenta
- **[CU-PG-003](Docs/Requerimientos/Casos%20de%20Uso/CU-PG-003%20Gestionar%20Datos%20Personales%20(Público%20General).md)**: Gestionar Datos Personales

### Gestión de Eventos

![alt](Docs/Requerimientos/Diagramas/img/Gestión%20de%20Eventos.png)

**Casos de uso relacionados:**
- **[CU-GE-001](Docs/Requerimientos/Casos%20de%20Uso/CU-GE-001%20Crear%20Evento.md)**: Crear Evento
- **[CU-GE-002](Docs/Requerimientos/Casos%20de%20Uso/CU-GE-002%20Consultar%20Eventos.md)**: Consultar Eventos
- **[CU-GE-003](Docs/Requerimientos/Casos%20de%20Uso/CU-GE-003%20Modificar%20Evento.md)**: Modificar Evento
- **[CU-GE-004](Docs/Requerimientos/Casos%20de%20Uso/CU-GE-004%20Eliminar%20Evento.md)**: Eliminar Evento
- **[CU-GE-005](Docs/Requerimientos/Casos%20de%20Uso/CU-GE-005%20Generar%20Constancias.md)**: Generar Constancias
- **[CU-GE-006](Docs/Requerimientos/Casos%20de%20Uso/CU-GE-006%20Generar%20Reportes%20de%20Eventos.md)**: Generar Reportes de Eventos
- **[CU-GE-007](Docs/Requerimientos/Casos%20de%20Uso/CU-GE-007%20Aprobar-Gestionar%20Solicitudes%20de%20Inscripción.md)**: Aprobar-Gestionar Solicitudes de Inscripción
- **[CU-GE-008](Docs/Requerimientos/Casos%20de%20Uso/CU-GE-008%20Validar%20Pagos%20Manuales.md)**: Validar Pagos Manuales

### Gestión de Categorías

![alt](Docs/Requerimientos/Diagramas/img/Gestión%20de%20Categorías.png)

**Casos de uso relacionados:**
- **[CU-GE-009](Docs/Requerimientos/Casos%20de%20Uso/CU-GE-009%20Crear%20Categoría%20de%20Evento-Capacitación.md)**: Crear Categoría de Evento-Capacitación
- **[CU-GE-010](Docs/Requerimientos/Casos%20de%20Uso/CU-GE-010%20Consultar%20Categorías%20de%20Evento-Capacitación.md)**: Consultar Categorías de Evento-Capacitación
- **[CU-GE-011](Docs/Requerimientos/Casos%20de%20Uso/CU-GE-011%20Modificar%20Categoría%20de%20Evento-Capacitación.md)**: Modificar Categoría de Evento-Capacitación
- **[CU-GE-012](Docs/Requerimientos/Casos%20de%20Uso/CU-GE-012%20Eliminar%20Categoría%20de%20Evento-Capacitación.md)**: Eliminar Categoría de Evento-Capacitación

---

## Módulo de Ventas (CRM)

*El módulo de ventas implementa un sistema CRM completo para la gestión de leads y oportunidades comerciales, desde la captación automática hasta el cierre de ventas.*

### Gestión de leads

![alt](Docs/Requerimientos/Diagramas/img/Gestión%20de%20Leads.png)

**Casos de uso relacionados:**
- **[CU-VE-001](Docs/Requerimientos/Casos%20de%20Uso/CU-VE-001%20Recuperar%20leads%20de%20fuentes%20externas.md)**: Recuperar leads de fuentes externas
- **[CU-VE-002](Docs/Requerimientos/Casos%20de%20Uso/CU-VE-002%20Agregar%20lead%20manualmente.md)**: Agregar lead manualmente
- **[CU-VE-003](Docs/Requerimientos/Casos%20de%20Uso/CU-VE-003%20Visualizar%20leads.md)**: Visualizar leads
- **[CU-VE-004](Docs/Requerimientos/Casos%20de%20Uso/CU-VE-004%20Asignar%20leads.md)**: Asignar leads
- **[CU-VE-005](Docs/Requerimientos/Casos%20de%20Uso/CU-VE-005%20Convertir%20lead%20en%20oportunidad.md)**: Convertir lead en oportunidad

### Gestión de oportunidades

![alt](Docs/Requerimientos/Diagramas/img/Gestión%20de%20Oportunidades.png)

**Casos de uso relacionados:**
- **[CU-VE-006](Docs/Requerimientos/Casos%20de%20Uso/CU-VE-006%20Registrar%20Interacción%20con%20Oportunidad.md)**: Registrar Interacción con Oportunidad
- **[CU-VE-007](Docs/Requerimientos/Casos%20de%20Uso/CU-VE-007%20Agendar%20Tarea%20de%20Seguimiento.md)**: Agendar Tarea de Seguimiento
- **[CU-VE-008](Docs/Requerimientos/Casos%20de%20Uso/CU-VE-008%20Cerrar%20Oportunidad%20Ganada-Perdida.md)**: Cerrar Oportunidad Ganada-Perdida
- **[CU-VE-009](Docs/Requerimientos/Casos%20de%20Uso/CU-VE-009%20Consultar%20recordatorios.md)**: Consultar recordatorios
- **[CU-VE-010](Docs/Requerimientos/Casos%20de%20Uso/CU-VE-010%20Gestionar%20Notificación%20de%20Recordatorio.md)**: Gestionar Notificación de Recordatorio
- **[CU-VE-011](Docs/Requerimientos/Casos%20de%20Uso/CU-VE-011%20Cargar%20Documentación%20en%20Nombre%20del%20Cliente.md)**: Cargar Documentación en Nombre del Cliente
- **[CU-VE-012](Docs/Requerimientos/Casos%20de%20Uso/CU-VE-012%20Consultar%20estado%20del%20pago.md)**: Consultar estado del pago

---

## Módulo de Usuarios

*Sistema integral para la administración de usuarios, capacitadores y validación de información personal y de facturación.*

### Usuarios

![alt](Docs/Requerimientos/Diagramas/img/Módulo%20de%20Usuarios.png)

**Casos de uso relacionados:**
- **[CU-MU-001](Docs/Requerimientos/Casos%20de%20Uso/CU-MU-001%20Consultar%20Usuarios.md)**: Consultar Usuarios
- **[CU-MU-002](Docs/Requerimientos/Casos%20de%20Uso/CU-MU-002%20Validar%20documentación.md)**: Validar documentación

### Gestión de Capacitadores

![alt](Docs/Requerimientos/Diagramas/img/Gestión%20de%20Capacitadores.png)

**Casos de uso relacionados:**
- **[CU-MU-003](Docs/Requerimientos/Casos%20de%20Uso/CU-MU-003%20Registrar%20Capacitador.md)**: Registrar Capacitador
- **[CU-MU-004](Docs/Requerimientos/Casos%20de%20Uso/CU-MU-004%20Consultar%20Capacitadores.md)**: Consultar Capacitadores
- **[CU-MU-005](Docs/Requerimientos/Casos%20de%20Uso/CU-MU-005%20Modificar%20Información%20de%20Capacitador.md)**: Modificar Información de Capacitador
- **[CU-MU-006](Docs/Requerimientos/Casos%20de%20Uso/CU-MU-006%20Archivar-Eliminar%20Capacitador.md)**: Archivar-Eliminar Capacitador
- **[CU-MU-007](Docs/Requerimientos/Casos%20de%20Uso/CU-MU-007%20Registrar-Actualizar%20Información%20de%20Pago-Facturación%20de%20Capacitador.md)**: Registrar-Actualizar Información de Pago-Facturación de Capacitador
- **[CU-MU-008](Docs/Requerimientos/Casos%20de%20Uso/CU-MU-008%20Validar%20Información%20de%20Pago-Facturación%20Propia.md)**: Validar Información de Pago-Facturación Propia
- **[CU-MU-009](Docs/Requerimientos/Casos%20de%20Uso/CU-MU-009%20Consultar%20Capacitaciones%20Asignadas.md)**: Consultar Capacitaciones Asignadas

### Administración de Usuarios

![alt](Docs/Requerimientos/Diagramas/img/Administración%20de%20Usuarios.png)

**Casos de uso relacionados:**
- **[CU-MU-001](Docs/Requerimientos/Casos%20de%20Uso/CU-MU-001%20Consultar%20Usuarios.md)**: Consultar Usuarios
- **[CU-MU-002](Docs/Requerimientos/Casos%20de%20Uso/CU-MU-002%20Validar%20documentación.md)**: Validar documentación

---

## Funcionalidades del Público General

*Interfaz y funcionalidades disponibles para los usuarios finales del sistema, desde la inscripción hasta el seguimiento de sus eventos.*

### Público General

![alt](Docs/Requerimientos/Diagramas/img/Público%20General.png)

**Casos de uso relacionados:**
- **[CU-PG-004](Docs/Requerimientos/Casos%20de%20Uso/CU-PG-004%20Solicitar%20Inscripción%20a%20Evento.md)**: Solicitar Inscripción a Evento
- **[CU-PG-005](Docs/Requerimientos/Casos%20de%20Uso/CU-PG-005%20Realizar%20Pago%20de%20Solicitud%20Aprobada.md)**: Realizar Pago de Solicitud Aprobada
- **[CU-PG-006](Docs/Requerimientos/Casos%20de%20Uso/CU-PG-006%20Cargar%20Documentos%20(por%20el%20usuario).md)**: Cargar Documentos (por el usuario)
- **[CU-PG-007](Docs/Requerimientos/Casos%20de%20Uso/CU-PG-007%20Consultar%20Estado%20de%20mis%20Solicitudes-Inscripciones.md)**: Consultar Estado de mis Solicitudes-Inscripciones
- **[CU-PG-008](Docs/Requerimientos/Casos%20de%20Uso/CU-PG-008%20Volver%20a%20Enviar%20Solicitud.md)**: Volver a Enviar Solicitud
- **[CU-PG-009](Docs/Requerimientos/Casos%20de%20Uso/CU-PG-009%20Consultar%20Mis%20Eventos.md)**: Consultar Mis Eventos

---

## Documentación Adicional

### Casos de Uso Detallados

Todos los casos de uso están documentados en detalle en la carpeta [`Docs/Requerimientos/Casos de Uso/`](Docs/Requerimientos/Casos%20de%20Uso/), donde cada archivo contiene:
- Descripción del caso de uso
- Actores involucrados
- Precondiciones y postcondiciones
- Flujo principal y flujos alternativos
- Criterios de aceptación

### Diagramas Fuente

Los diagramas están disponibles en formato PlantUML en [`Docs/Requerimientos/Diagramas/`](Docs/Requerimientos/Diagramas/) para facilitar su edición y mantenimiento.

---

## Estimación de Requerimientos

El método de estimación utilizado en este proyecto es un sistema de clasificación cualitativa personalizado que evalúa la complejidad de los casos de uso mediante tres dimensiones técnicas clave: 

- **Interacciones backend/frontend** (1-2 para sencillo, 3-5 para mediano, 6+ para complicado)
- **Operaciones CRUD** (1-2 operaciones simples vs. lógica avanzada) 
- **Interfaces requeridas** (1-2 interfaces básicas vs. múltiples estados complejos)

Este enfoque específico para desarrollo web permite clasificar cada funcionalidad en tres categorías (Sencillo, Mediano, Complicado) con justificaciones detalladas, considerando tanto la arquitectura del sistema como la experiencia de usuario. 

**Resultados del análisis** (42 casos de uso):
- 📊 **59.5%** Sencillos
- 📊 **35.7%** Medianos  
- 📊 **4.8%** Complicados

Las funcionalidades más complejas identificadas involucran integraciones externas (pagos y APIs de terceros), lo que proporciona al equipo una base sólida para la planificación y asignación de recursos del proyecto.

📄 **Documentación completa:** [Estimación](Docs/Requerimientos/Estimación.md)
