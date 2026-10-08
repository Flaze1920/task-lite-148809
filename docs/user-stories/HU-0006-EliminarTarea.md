#HU-0006-Eliminar tareas
## Historia de usuario

Como integrante del equipo quiero eliminar una tarea, para retirar del sistema aquellas que ya no necesitan seguimiento o fueron creadas por error

## Criterios de Aceptacion

### CA-001- Solicitud de confirmacion
Given que el usuario selecciona eliminar una tarea
When realiza la accion
Then el sistema debe solicitar una confirmacion antes de proceder con el borrado

### CA-002- Eliminacion exitosa
Given que el usuario confirmo la eliminacion de una tarea
When el sistema procesa la solicitud
Then la tarea debe ser eliminada
And ya no debe mostrarse en la lista general de tareas

### CA-003- Cancelar eliminacion
Given que el sistema solicito confirmacion para eliminar una tarea
When el usuario decide cancelar la accion
Then la tarea no debe ser eliminada
And debe permanecer intacta en la lista general

## Reglas del Negocio
RN-001: La accion de eliminar debe ser confirmada explicitamente por el usuario para evitar borrados accidentales.
RN-002: Una vez eliminada, la tarea se remueve definitivamente del sistema y no puede recuperarse.
RN-003: Se puede eliminar una tarea sin importar su estado actual.

## Dependencias
Esta historia depende de HU-0002 para poder visualizar y seleccionar la tarea especifica que se desea eliminar.

## Fuera del Alcance
* Papelera de reciclaje.
* Archivo historico de tareas borradas.
* Eliminacion masiva (borrar varias tareas al mismo tiempo).
* Borrado automatico de tareas despues de cierto tiempo.