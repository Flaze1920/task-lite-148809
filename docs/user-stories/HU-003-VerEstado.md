#HU-0003-Consultar estado de las tareas
## Historia de usuario

Como integrante del equipo quiero identificar rapidamente el estado de cada tarea, para conocer su situacion actual de un solo vistazo

## Criterios de Aceptacion

### CA-001- Estados validos
Given que el usuario visualiza una tarea
When consulta cual es su estado
Then el valor debe corresponder unicamente a Pendiente, En progreso, Terminada o Cancelada

### CA-002- Distincion visual del estado
Given que existen tareas en la lista general
When el usuario observa la informacion de la tarea
Then el estado debe contar con una apariencia o formato visual unico
And debe permitir distinguirlo facilmente de los otros estados posibles

### CA-003- Lista unificada
Given que existen multiples tareas con diferentes estados
When se despliega la lista general
Then las tareas deben permanecer juntas en una sola lista
And no deben separarse por columnas ni tableros

## Reglas del Negocio
RN-001: El ciclo de vida de la tarea se compone de 4 estados fijos: Pendiente, En progreso, Terminada, Cancelada.
RN-002: Cada estado debe tener una caracteristica visual diferente (ej. color) para ser reconocido rapidamente.
RN-003: La distincion de estados es puramente visual y no modifica la estructura de una sola lista definida en la vista principal.

## Dependencias
Esta historia depende de HU-0002-Visualizar tareas, ya que requiere que la lista general exista para poder aplicar la distincion visual a los textos.

## Fuera del Alcance
* Cambiar o actualizar el estado de una tarea (se hara en otra HU).
* Tableros tipo Kanban o multiples columnas.
* Agrupar las tareas segun su estado.
* Filtrar tareas por estado (se hara en otra HU).