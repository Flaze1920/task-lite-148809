#HU-0005-Editar informacion de una tarea
## Historia de usuario

Como integrante del equipo quiero editar la informacion de una tarea registrada, para corregir o actualizar sus detalles sin necesidad de volver a crearla

## Criterios de Aceptacion

### CA-001- Edicion exitosa
Given que el usuario selecciona editar una tarea
When modifica el titulo o descripcion con valores validos
And guarda los cambios
Then la informacion de la tarea debe actualizarse correctamente
And debe verse reflejada en la vista general

### CA-002- Validacion del titulo editado
Given que el usuario esta editando una tarea
When intenta guardar los cambios dejando el titulo vacio o fuera de la longitud permitida (3 a 80 caracteres)
Then la edicion no debe guardarse
And debe recibir informacion indicando el error en el titulo

### CA-003- Validacion de la descripcion editada
Given que el usuario esta editando una tarea
When intenta guardar los cambios con una descripcion mayor a 300 caracteres
Then la edicion no debe guardarse
And debe informarse la restriccion correspondiente

### CA-004- Cancelar edicion
Given que el usuario esta editando una tarea y realiza cambios
When decide cancelar la edicion
Then los cambios no deben guardarse
And la tarea debe conservar su informacion original

## Reglas del Negocio
RN-001: Solo se puede editar el titulo y la descripcion de la tarea.
RN-002: El titulo editado sigue siendo obligatorio y debe tener entre 3 y 80 caracteres.
RN-003: La descripcion editada sigue siendo opcional y tendra un maximo de 300 caracteres.
RN-004: Se puede editar la informacion de una tarea sin importar su estado actual.

## Dependencias
Esta historia depende de HU-0001 (para la estructura de datos y reglas de validacion) y HU-0002 (para ubicar la tarea a editar).

## Fuera del Alcance
* Editar el estado de la tarea (cubierto en HU-0004).
* Guardar un historial de versiones o ediciones anteriores.
* Recuperar informacion sobrescrita por error.
* Edicion simultanea o colaborativa por varias personas.