#HU-0002-Visualizar tareas
## Historia de usuario

Como integrante del equipo quiero visualizar las tareas registradas, para consultar de forma clara el trabajo existente y su estado actual

## Criterios de Aceptacion

### CA-001-Visualizar lista de tareas
Given que existen tareas registradas en el sistema
When el usuario ingresa a la vista de tareas
Then debe poder ver la lista completa
And cada tarea debe mostrar su titulo y su estado actual

### CA-002-Lista sin tareas
Given que no existen tareas registradas
When el usuario ingresa a la vista de tareas
Then no debe mostrarse ninguna tarea
And debe recibir informacion visual indicando que no hay tareas registradas

### CA-003-Orden de visualizacion
Given que existen multiples tareas registradas
When el usuario visualiza la lista
Then las tareas deben mostrarse ordenadas cronologicamente
And las tareas mas recientes deben aparecer al principio

### CA-004-Persistencia visual de la descripcion
Given que una tarea fue registrada con descripcion
When el usuario visualiza la tarea en la lista general
Then la descripcion no debe mostrarse en esta vista resumida

## Reglas del Negocio
RN-001: La informacion visible por tarea debe ser unicamente el titulo y el estado.
RN-002: Si el sistema no tiene tareas, debe notificar al usuario que la lista esta vacia.
RN-003: El orden de las tareas es descendente respecto a su fecha de creacion (mas recientes primero).

## Dependencias
Esta historia depende de HU-0001-CrearTarea para poder contar con datos reales que mostrar en el sistema.

## Fuera del Alcance
* Paginacion de los resultados.
* Buscar tareas especificas (se hara en otra HU).
* Filtrar tareas por estado (se hara en otra HU).
* Ver la descripcion detallada de la tarea en una vista individual.