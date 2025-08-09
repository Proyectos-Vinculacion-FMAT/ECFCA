**Nombre del Caso de Uso:** Modificar Categoría de Evento/Capacitación

**ID:** CU-GE-011

**Actor(es):** Administrativo

**Descripción:** El administrativo actualiza el nombre de una categoría de evento/capacitación existente.

**Precondiciones:**

* El Administrativo ha iniciado sesión en el sistema.
* La categoría a modificar existe en el sistema.

**Flujo Básico (Camino Feliz):**

1. El Administrativo accede a la sección de "Gestión de Categorías".
2. El Administrativo selecciona la categoría que desea modificar de la lista.
3. El sistema presenta un campo editable con el nombre actual de la categoría.
4. El Administrativo edita el nombre de la categoría.
5. El Administrativo guarda los cambios.
6. El sistema confirma la modificación y actualiza la categoría en la lista.

**Flujos Alternativos y Excepciones:**

* **Alternativa A:** El Administrativo decide cancelar la modificación.
* **Excepción B:** El nuevo nombre de la categoría ya existe. El sistema notifica al Administrativo sobre el nombre duplicado.
* **Excepción C:** El nuevo nombre de la categoría está vacío o es inválido. El sistema solicita un nombre válido.

**Post-condiciones:**

* El nombre de la categoría ha sido actualizado en el sistema.
* Los eventos/capacitaciones asociados a esa categoría reflejarán el nuevo nombre.