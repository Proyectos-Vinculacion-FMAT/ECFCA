**Nombre del Caso de Uso:** Crear Evento

**ID:** CU-GE-001

**Actor(es):** Administrativo

**Descripción:** El administrativo crea un nuevo evento en el sistema, especificando sus detalles como nombre, fechas, modalidad y precios.

**Precondiciones:**

* El Administrativo ha iniciado sesión en el sistema.
* El Administrativo tiene los permisos necesarios para gestionar eventos.

**Flujo Básico (Camino Feliz):**

1. El Administrativo selecciona la opción "Crear evento" dentro de la "Gestión de eventos".
2. El sistema presenta un formulario para ingresar los detalles del evento.
3. El Administrativo ingresa los datos del evento.
4. El Administrativo guarda el nuevo evento.
5. El sistema confirma la creación del evento y lo lista en la gestión de eventos.

**Flujos Alternativos y Excepciones:**

* **Alternativa A:** El Administrativo decide cancelar la creación del evento en cualquier momento antes de guardar.
* **Excepción B:** Faltan campos obligatorios al intentar guardar el evento. El sistema indica los campos faltantes.
* **Excepción C:** Las fechas de inicio y fin son inválidas (ej. fecha de fin anterior a la de inicio). El sistema muestra un mensaje de error.

**Post-condiciones:**

* Se ha creado un nuevo evento en el sistema con el estado "Pendiente" o "Borrador".
* El evento es visible en la lista de eventos.