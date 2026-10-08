#HU-0004-Actualizar estado de una tarea
## Historia de usuario

Como integrante del equipo quiero actualizar el estado de una tarea, para mantener actualizada la situacion de cada tarea conforme avanza el trabajo

## Criterios de Aceptacion

### CA-001- Actualizacion exitosa
Given que el usuario visualiza una tarea registrada
When selecciona un nuevo estado valido para dicha tarea
Then el sistema debe guardar el cambio
And la lista debe reflejar el nuevo estado inmediatamente

### CA-002- Opciones de estado disponibles
Given que el usuario desea modificar el estado de una tarea
When consulta las opciones disponibles
Then solo debe poder elegir entre Pendiente, En progreso, Terminada y Cancelada

### CA-003- Transicion libre de estados
Given que una tarea tiene un estado actual
When el usuario decide cambiarla a cualquier otro de los estados permitidos
Then la actualizacion debe realizarse sin bloqueos ni requerir un orden especifico

### CA-004- Seleccion del mismo estado
Given que una tarea tiene un estado actual
When el usuario selecciona el mismo estado que ya tenia
Then el sistema no debe realizar ninguna accion ni mostrar error

## Reglas del Negocio
RN-001: El estado de una tarea puede actualizarse multiples veces a lo largo de su ciclo de vida.
RN-002: Los valores permitidos para actualizacion son unicamente los definidos: Pendiente, En progreso, Terminada, Cancelada.
RN-003: No existe un flujo estricto; cualquier estado puede cambiar a cualquier otro estado.

## Dependencias
Esta historia depende de HU-0001 (para tener tareas creadas) y esta fuertemente vinculada a HU-0002 y HU-0003, ya que la actualizacion se realizara e impactara visualmente en la lista de tareas.

## Fuera del Alcance
* Guardar un historial o bitacora de los cambios de estado.
* Restricciones o flujos forzados entre estados (ej. no poder reabrir tareas).
* Notificaciones por correo o sistema al cambiar de estado.
* Registrar el usuario o la fecha y hora exacta del cambio de estado.