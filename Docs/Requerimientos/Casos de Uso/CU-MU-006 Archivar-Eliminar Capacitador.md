**Nombre del Caso de Uso:** Archivar/Eliminar Capacitador

**ID:** CU-MU-006

**Actor(es):** Administrativo

**Descripción:** El administrativo archiva o elimina un registro de capacitador del sistema.

**Precondiciones:**

* El Administrativo ha iniciado sesión en el sistema.
* El capacitador existe en el sistema.

**Flujo Básico (Camino Feliz):**

1. El Administrativo accede al "Módulo de Usuarios" y selecciona la opción "Gestionar Capacitadores".
2. El Administrativo selecciona el capacitador que desea archivar/eliminar de la lista.
3. El sistema solicita una confirmación al Administrativo.
4. El Administrativo confirma la acción.
5. El sistema cambia el estado del capacitador a "Archivado" o lo elimina completamente.

**Flujos Alternativos y Excepciones:**

* **Alternativa A:** El Administrativo cancela la operación.
* **Excepción B:** El capacitador tiene eventos/capacitaciones asignadas activas. El sistema notifica al Administrativo y no permite la eliminación directa, sugiriendo reasignar o archivar primero los eventos.
* **Excepción C:** Error del sistema al intentar archivar/eliminar.

**Post-condiciones:**

* El capacitador ya no es visible en las listas activas o ha sido removido del sistema.
* (Si aplica) Los eventos/capacitaciones donde estaba asignado el capacitador reflejan su estado (ej. "Capacitador archivado" o campo vacío).