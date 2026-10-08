#HU-0008-Buscar tareas
## Historia de usuario

Como integrante del equipo quiero buscar tareas mediante una entrada de texto, para encontrar rapidamente una tarea especifica cuando la cantidad total aumente

## Criterios de Aceptacion

### CA-001- Busqueda con coincidencias
Given que existen tareas registradas en el sistema
When el usuario ingresa un termino de busqueda
Then la lista debe actualizarse mostrando unicamente las tareas cuyo titulo o descripcion contengan el termino ingresado

### CA-002- Busqueda sin resultados
Given que el usuario ingresa un termino de busqueda
When el sistema evalua las tareas registradas
And ninguna tarea contiene el termino en su titulo ni en su descripcion
Then la lista debe quedar vacia
And debe mostrarse un mensaje indicando que no se encontraron coincidencias

### CA-003- Sensibilidad de caracteres
Given que existen tareas con mayusculas y minusculas en su informacion
When el usuario ingresa un termino de busqueda ignorando estas diferencias
Then el sistema debe encontrar las coincidencias de igual manera (case-insensitive)

### CA-004- Limpiar busqueda
Given que el usuario tiene resultados de busqueda activos en la pantalla
When borra el termino de busqueda del campo
Then la lista debe regresar a su estado original mostrando las tareas sin el criterio de busqueda

## Reglas del Negocio
RN-001: La busqueda de texto abarcara unicamente los campos de titulo y descripcion.
RN-002: La busqueda debe ignorar diferencias entre mayusculas y minusculas.
RN-003: Al limpiar el texto de busqueda, la lista recupera la visualizacion de las tareas previas.

## Dependencias
Esta historia depende de HU-0002 para poder renderizar los resultados en la lista general. Tambien interactua con HU-0007, pendiente de definir si se combinan o son excluyentes.

## Fuera del Alcance
* Busqueda avanzada por expresiones regulares
* Busqueda aproximada 
* Resaltar visualmente la palabra encontrada dentro del texto de la tarea.