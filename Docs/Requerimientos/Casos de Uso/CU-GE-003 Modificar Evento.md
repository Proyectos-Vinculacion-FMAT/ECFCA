**Nombre del Caso de Uso:** Modificar Evento

**ID:** CU-GE-003

**Actor(es):** Administrativo

**Descripción:** El administrativo actualiza la información de un evento existente en el sistema.

**Precondiciones:**

* El Administrativo ha iniciado sesión en el sistema.
* El evento a modificar existe en el sistema.

**Flujo Básico (Camino Feliz):**

1. El Administrativo selecciona la opción "Modificar evento" o un icono de edición junto a un evento en la lista de eventos (previa consulta, CU-GE-002).
2. El sistema muestra un formulario pre-llenado con la información actual del evento.
3. El Administrativo realiza los cambios necesarios en los campos del evento (nombre, fechas, modalidad, precios, etc.).
4. El Administrativo guarda los cambios.
5. El sistema actualiza la información del evento y confirma la modificación.

**Flujos Alternativos y Excepciones:**

* **Alternativa A:** El Administrativo decide cancelar la modificación en cualquier momento antes de guardar.
* **Excepción B:** Faltan campos obligatorios o los datos son inválidos (ej. fechas inconsistentes) al intentar guardar. El sistema resalta los errores.
* **Excepción C:** El evento ha tenido inscripciones y ciertos campos (ej. modalidad, fechas ya pasadas) no pueden ser modificados.

**Post-condiciones:**

* La información del evento ha sido actualizada en el sistema.