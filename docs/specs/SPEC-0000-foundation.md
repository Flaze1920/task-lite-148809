# SPEC-000 – Foundation

## Propósito

Definir la base técnica y las convenciones iniciales de **TaskFlow Lite**, estableciendo una estructura simple y mantenible para desarrollar posteriormente las capacidades del producto.

Esta especificación busca asegurar que el proyecto pueda ejecutarse localmente desde VSCode y evolucionar de forma incremental sin incorporar complejidad técnica innecesaria.

---

## Alcance

Esta especificación contempla únicamente:

* Definición de la estructura inicial del proyecto.
* Organización del código dentro de `src/`.
* Definición de las tecnologías permitidas.
* Definición de convenciones de nombres.
* Definición de convenciones básicas de Git.
* Definición de una Definition of Done técnica inicial.
* Preparación para una futura persistencia mediante `localStorage`.

No se implementarán todavía historias funcionales ni capacidades de gestión de tareas.

---

## Estructura inicial del proyecto

La estructura inicial deberá organizarse de la siguiente manera:

```text
TaskFlow-Lite/
├── src/
│   ├── index.html
│   ├── css/
│   └── js/
├── .gitignore
└── SPEC-000-foundation.md
```

La carpeta `src/` contendrá el código fuente de la aplicación.

La organización interna podrá ampliarse conforme se incorporen nuevas funcionalidades, siempre manteniendo una estructura simple y coherente con el crecimiento del proyecto.

---

## Restricciones técnicas

* Se utilizará **HTML5** para la estructura de las páginas.
* Se utilizará **CSS3** para los estilos y presentación visual.
* Se utilizará **JavaScript ES Modules** para la lógica de la aplicación.
* No se utilizarán frameworks de frontend.
* No se utilizará backend.
* No se utilizarán bases de datos externas.
* La persistencia de datos se realizará posteriormente mediante `localStorage`.
* El proyecto deberá poder ejecutarse localmente desde **VSCode**.
* No se incorporarán dependencias o herramientas adicionales sin que exista una necesidad definida.
* Las funcionalidades se desarrollarán de manera incremental.
* Esta etapa no contempla la implementación de historias funcionales.

---

## Convenciones de nombres

Se utilizarán nombres descriptivos y consistentes.

### Archivos

* Archivos HTML: `kebab-case.html`
* Archivos CSS: `kebab-case.css`
* Archivos JavaScript: `kebab-case.js`

Ejemplos:

```text
index.html
task-list.css
task-service.js
```

### Variables y funciones

JavaScript utilizará `camelCase` para variables y funciones.

Ejemplos conceptuales:

```text
taskList
createTask
updateTaskStatus
```

### Constantes

Las constantes globales o valores que representen configuraciones constantes utilizarán `UPPER_SNAKE_CASE`.

Ejemplo:

```text
STORAGE_KEY
```

### Carpetas

Las carpetas utilizarán `kebab-case` y nombres descriptivos.

---

## Convenciones de Git

Se utilizará Git para controlar las versiones del proyecto.

Los commits deberán ser pequeños y representar cambios concretos.

Se utilizará la siguiente convención básica para los mensajes de commit:

```text
tipo: descripción breve
```

Tipos iniciales permitidos:

* `feat`: nueva funcionalidad.
* `fix`: corrección de un problema.
* `refactor`: modificación interna sin cambiar el comportamiento esperado.
* `style`: cambios de formato o estilos.
* `docs`: cambios en documentación.
* `chore`: tareas de mantenimiento.

Ejemplos:

```text
feat: agregar estructura inicial
docs: agregar especificacion foundation
style: ajustar estilos base
```

No se deberán mezclar cambios no relacionados dentro de un mismo commit cuando puedan separarse razonablemente.

---

## Definition of Done técnica inicial

La fundación técnica se considerará terminada cuando:

* La estructura inicial del proyecto esté creada.
* El código fuente se encuentre organizado dentro de `src/`.
* HTML5, CSS3 y JavaScript ES Modules sean las tecnologías utilizadas.
* No existan frameworks ni backend.
* El proyecto pueda abrirse y ejecutarse localmente desde VSCode.
* Las convenciones de nombres estén definidas y sean aplicables al proyecto.
* Las convenciones básicas de Git estén documentadas.
* La estructura permita incorporar posteriormente `localStorage`.
* La especificación `SPEC-000-foundation.md` esté documentada.
* No se hayan implementado historias funcionales como parte de esta fundación.

---

## Fuera de alcance

Queda fuera de esta especificación:

* Registro de tareas.
* Visualización funcional de tareas.
* Actualización de tareas.
* Gestión de estados de tareas.
* Edición o eliminación de tareas.
* Búsqueda o filtrado de tareas.
* Implementación de `localStorage`.
* Backend o API.
* Base de datos.
* Autenticación de usuarios.
* Frameworks o librerías de frontend.
* Diseño funcional completo de la interfaz.
* Historias de usuario.
* Pruebas funcionales de las capacidades del producto.

Estas funcionalidades podrán abordarse posteriormente mediante especificaciones e incrementos independientes.
