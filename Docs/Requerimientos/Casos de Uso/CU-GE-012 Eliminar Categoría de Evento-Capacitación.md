**Nombre del Caso de Uso:** Eliminar Categoría de Evento/Capacitación

**ID:** CU-GE-012

**Actor(es):** Administrativo

**Descripción:** El administrativo elimina una categoría de evento/capacitación del sistema.

**Precondiciones:**

* El Administrativo ha iniciado sesión en el sistema.
* La categoría a eliminar existe en el sistema.
* La categoría no está siendo utilizada por ningún evento o capacitación (o se maneja una reasignación/eliminación en cascada).

**Flujo Básico (Camino Feliz):**

1. El Administrativo accede a la sección de "Gestión de Categorías".
2. El Administrativo selecciona la categoría que desea eliminar de la lista.
3. El sistema solicita una confirmación al Administrativo.
4. El Administrativo confirma la eliminación.
5. El sistema elimina la categoría y la retira de la lista.

**Flujos Alternativos y Excepciones:**

* **Alternativa A:** El Administrativo cancela la eliminación.
* **Excepción B:** La categoría está siendo utilizada por uno o más eventos/capacitaciones. El sistema notifica al Administrativo y le impide la eliminación directa, sugiriendo reasignar los eventos a otra categoría primero.
* **Excepción C:** Error del sistema al intentar eliminar la categoría.

**Post-condiciones:**

* La categoría ha sido eliminada del sistema.
* (Si aplica) Los eventos/capacitaciones previamente asociados a esa categoría no tendrán categoría o se les asignará una por defecto.