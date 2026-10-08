#HU-0007-Filtrar tareas
## Historia de usuario

Como integrante del equipo quiero filtrar las tareas de la lista segun su estado, para localizar rapidamente el grupo de tareas que necesito revisar

## Criterios de Aceptacion

### CA-001- Aplicar filtro por estado
Given que existen tareas con diferentes estados en la lista general
When el usuario selecciona un estado especifico para filtrar (ej. Pendiente)
Then la lista debe actualizarse para mostrar unicamente las tareas que coincidan con ese estado
And las tareas que tengan otros estados deben ocultarse

### CA-002- Filtro sin resultados
Given que el usuario aplica un filtro por un estado
And no existe ninguna tarea con ese estado actual
When se actualiza la lista
Then no debe mostrarse ninguna tarea
And debe aparecer un mensaje indicando que no hay tareas con el estado seleccionado

### CA-003- Limpiar filtro
Given que el usuario tiene un filtro activo aplicado en la lista
When selecciona la opcion de limpiar el filtro o ver "Todas"
Then la lista debe actualizarse para mostrar nuevamente todas las tareas registradas
And debe mantenerse el orden cronologico original

## Reglas del Negocio
RN-001: El filtrado operara basandose unicamente en los 4 estados definidos (Pendiente, En progreso, Terminada, Cancelada).
RN-002: Por defecto, al ingresar al sistema, no habra ningun filtro activo (se muestran todas las tareas).
RN-003: Al aplicar un filtro, las tareas resultantes mantienen su orden descendente por fecha de creacion.

## Dependencias
Esta historia depende de HU-0002 para la lista y de HU-0003 para los estados de las tareas.

## Fuera del Alcance
* Filtrar por fecha de creacion.
* Filtrar tareas combinando multiples estados al mismo tiempo.
* Busqueda por texto (esto se abordara en la HU-0008).
* Guardar el filtro activo si el usuario recarga la pagina o cierra el navegador.