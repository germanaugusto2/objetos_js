# Date

## Que es Date?

- En JavaScript, Date es un objeto incorporado que representa una fecha y hora. Puedes usar el objeto Date para trabajar con fechas y horas en tu código JavaScript. Puedes crear un nuevo objeto Date de varias maneras, como especificar una fecha y hora específicas, o simplemente crear un objeto Date que represente el momento actual.

Aquí tienes un ejemplo básico de cómo crear un objeto Date en JavaScript:


```Javascript
// Crear un objeto Date que represente el momento actual
var fechaActual = new Date();

// Crear un objeto Date con una fecha específica (año, mes, día)
var fechaEspecifica = new Date(2024, 3, 22); // El mes se indexa desde 0, por lo que 3 representa abril

// También puedes especificar la hora, minutos, segundos y milisegundos
var fechaConHora = new Date(2024, 3, 22, 10, 30, 0); // 10:30 AM

// Obtener diferentes componentes de la fecha
var año = fechaActual.getFullYear();
var mes = fechaActual.getMonth(); // ¡Recuerda que los meses se indexan desde 0!
var día = fechaActual.getDate();
var hora = fechaActual.getHours();
var minutos = fechaActual.getMinutes();
var segundos = fechaActual.getSeconds();
var milisegundos = fechaActual.getMilliseconds();

// Obtener la fecha y hora actual en formato de cadena de texto
var fechaHoraActual = fechaActual.toString();

// También puedes realizar operaciones como establecer una nueva fecha
fechaActual.setFullYear(2025); // Establecer el año a 2025
```
## Para que sirve?

- El objeto Date en JavaScript sirve para manejar fechas y horas en tus aplicaciones web. Aquí hay algunas formas en las que puedes utilizar el objeto Date:

    - Obtener la fecha y hora actual: Puedes crear un objeto Date sin argumentos para obtener la fecha y hora actuales del sistema.
    - Crear fechas específicas: Puedes crear objetos Date para representar fechas y horas específicas, útiles para programar eventos o tareas futuras.
    - Manipular fechas: El objeto Date proporciona métodos para manipular fechas, como establecer y obtener el año, mes, día, hora, minutos, segundos, etc.
    - Formatear fechas: Puedes convertir objetos Date en cadenas de texto en diferentes formatos para mostrar fechas de manera legible para los usuarios.
    - Realizar cálculos de tiempo: Puedes realizar operaciones matemáticas con fechas, como sumar o restar días, horas, minutos, etc.
    - Trabajar con zonas horarias: El objeto Date permite trabajar con zonas horarias, aunque es importante tener en cuenta que JavaScript maneja las zonas horarias de manera limitada en comparación con otros lenguajes.

## En que se utiliza o en donde se puede usar?


- El objeto Date en JavaScript se puede utilizar en una amplia variedad de contextos y escenarios dentro del desarrollo web y de aplicaciones. Aquí hay algunas áreas donde se puede usar el objeto Date:

    - Desarrollo web: En el desarrollo web, el objeto Date se utiliza comúnmente para mostrar la fecha y hora actual en páginas web dinámicas. Por ejemplo, puedes mostrar la fecha y hora de publicación de un artículo, la fecha y hora de un evento próximo, o mostrar un reloj en tiempo real en una página web.
    - Formularios y entradas de usuario: Los formularios web pueden incluir campos de fecha y hora donde los usuarios pueden seleccionar una fecha y hora específicas. El objeto Date se puede utilizar para validar y procesar las entradas de fecha y hora del usuario.
    - Aplicaciones de calendario y programación: En aplicaciones de calendario, planificación y programación, el objeto Date se utiliza para manejar eventos, tareas y recordatorios. Puedes calcular fechas futuras, establecer recordatorios y gestionar horarios utilizando el objeto Date.
    - Animaciones y efectos visuales: En el desarrollo de juegos y animaciones web, el objeto Date se puede utilizar para sincronizar eventos y efectos visuales con el tiempo. Por ejemplo, puedes crear animaciones que ocurran en momentos específicos del día o que cambien según la hora actual.
    - Aplicaciones de comercio electrónico: En aplicaciones de comercio electrónico, el objeto Date se puede utilizar para mostrar fechas de entrega estimadas, tiempos de oferta limitada y otras información temporal relevante para los usuarios.
    - Aplicaciones de seguimiento y registro: En aplicaciones de seguimiento y registro, el objeto Date se puede utilizar para registrar la fecha y hora en que ocurrieron eventos específicos, como registros de inicio de sesión, transacciones financieras, o actualizaciones de estado.

## En que nos ayuda?

- El objeto Date en JavaScript ofrece varias formas en las que puede ayudar en el desarrollo de aplicaciones. Aquí hay algunas formas específicas en las que puede ser útil:

    - Gestión del tiempo: El objeto Date permite manipular fechas y horas, lo que es esencial para muchas aplicaciones que necesitan gestionar eventos temporales. Puedes realizar cálculos de tiempo, como sumar o restar días, calcular la diferencia entre dos fechas, y más.
    - Interacción con el usuario: Cuando necesitas que los usuarios interactúen con fechas y horas, el objeto Date te permite crear interfaces de usuario que incluyan selección de fechas, control de tiempo, o mostrar la hora actual en tiempo real.
    - Programación de eventos y tareas: Para aplicaciones que involucran planificación, como calendarios o aplicaciones de tareas, el objeto Date es esencial para programar eventos, establecer recordatorios y gestionar horarios.
    - Personalización y formato de fechas: Puedes utilizar el objeto Date para formatear fechas y horas de acuerdo con las preferencias del usuario o los estándares de presentación específicos de tu aplicación. Esto es útil para mostrar información de manera legible y coherente.
    - Sincronización temporal: En aplicaciones que requieren sincronización con el tiempo del sistema o eventos específicos, el objeto Date te permite realizar acciones basadas en el tiempo, como activar funciones en momentos específicos o sincronizar animaciones y efectos visuales.
    - Registro de eventos: Para aplicaciones que necesitan rastrear y registrar eventos en el tiempo, como registros de actividad, transacciones financieras o actualizaciones de estado, el objeto Date te permite capturar y almacenar la fecha y hora en que ocurrieron esos eventos.

## Ejemplo basico

```Javascript
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Validar Fecha</title>
</head>
<body>
    <h1>Validar Fecha</h1>
    <form onsubmit="return validarFecha()">
        <label for="fecha">Ingrese una fecha:</label>
        <input type="date" id="fecha" required>
        <button type="submit">Validar</button>
    </form>

    <script>
        function validarFecha() {
            var fechaIngresada = new Date(document.getElementById('fecha').value);

            if (isNaN(fechaIngresada.getTime())) {
                alert("Por favor, ingrese una fecha válida.");
                return false;
            }

            alert("La fecha ingresada es: " + fechaIngresada.toDateString());
            return true;
        }
    </script>
</body>
</html>
```

## Propiedades 

- El objeto Date en JavaScript tiene varias propiedades y métodos que permiten trabajar con fechas y horas de manera efectiva. Aquí tienes algunas de las principales propiedades y métodos del objeto Date:

    - Date.prototype.constructor: Devuelve la función constructora de un objeto Date.
    - Date.prototype.getDate(): Devuelve el día del mes (del 1 al 31) de un objeto Date.
    - Date.prototype.getDay(): Devuelve el día de la semana (del 0 al 6, donde 0 es domingo) de un objeto Date.
    - Date.prototype.getFullYear(): Devuelve el año (como un número de cuatro dígitos) de un objeto Date.
    - Date.prototype.getHours(): Devuelve la hora (del 0 al 23) de un objeto Date.
    - Date.prototype.getMilliseconds(): Devuelve los milisegundos (del 0 al 999) de un objeto Date.
    - Date.prototype.getMinutes(): Devuelve los minutos (del 0 al 59) de un objeto Date.
    - Date.prototype.getMonth(): Devuelve el mes (del 0 al 11, donde 0 es enero) de un objeto Date.
    - Date.prototype.getSeconds(): Devuelve los segundos (del 0 al 59) de un objeto Date.
    - Date.prototype.getTime(): Devuelve el número de milisegundos desde el 1 de enero de 1970 (Epoch) hasta la fecha/hora representada por el objeto Date.
    - Date.prototype.getTimezoneOffset(): Devuelve la diferencia de tiempo, en minutos, entre la hora local y la hora UTC (Tiempo Universal Coordinado).
    - Date.prototype.getUTCDate(): Devuelve el día del mes (del 1 al 31) de un objeto Date según la hora UTC.
    - Date.prototype.getUTCDay(): Devuelve el día de la semana (del 0 al 6, donde 0 es domingo) de un objeto Date según la hora UTC.
    - Date.prototype.getUTCFullYear(): Devuelve el año (como un número de cuatro dígitos) de un objeto Date según la hora UTC.
    - Date.prototype.getUTCHours(): Devuelve la hora (del 0 al 23) de un objeto Date según la hora UTC.
    - Date.prototype.getUTCMilliseconds(): Devuelve los milisegundos (del 0 al 999) de un objeto Date según la hora UTC.
    - Date.prototype.getUTCMinutes(): Devuelve los minutos (del 0 al 59) de un objeto Date según la hora UTC.
    - Date.prototype.getUTCMonth(): Devuelve el mes (del 0 al 11, donde 0 es enero) de un objeto Date según la hora UTC.
    - Date.prototype.getUTCSeconds(): Devuelve los segundos (del 0 al 59) de un objeto Date según la hora UTC.

## Metodos

- Diferentes metodos

    - Date.now(): Devuelve el número de milisegundos transcurridos desde el 1 de enero de 1970 (Epoch) hasta la invocación del método.
    - Date.parse(): Analiza una cadena de texto y devuelve el número de milisegundos desde el 1 de enero de 1970 (Epoch) hasta la fecha representada por la cadena.
    - Date.UTC(): Acepta argumentos similares a los de la función constructora Date(), pero devuelve el número de milisegundos desde el 1 de enero de 1970 (Epoch) en la hora UTC.
    - Date.prototype.setDate(): Establece el día del mes de un objeto Date según el valor proporcionado.
    - Date.prototype.setFullYear(): Establece el año de un objeto Date según el valor proporcionado.
    - Date.prototype.setHours(): Establece la hora de un objeto Date según el valor proporcionado.
    - Date.prototype.setMilliseconds(): Establece los milisegundos de un objeto Date según el valor proporcionado.
    - Date.prototype.setMinutes(): Establece los minutos de un objeto Date según el valor proporcionado.
    - Date.prototype.setMonth(): Establece el mes de un objeto Date según el valor proporcionado.
    - Date.prototype.setSeconds(): Establece los segundos de un objeto Date según el valor proporcionado.
    - Date.prototype.setTime(): Establece un objeto Date a la hora representada por el número de milisegundos desde el 1 de enero de 1970 (Epoch).
    - Date.prototype.setUTCDate(): Establece el día del mes de un objeto Date según el valor proporcionado, en la hora UTC.
    - Date.prototype.setUTCFullYear(): Establece el año de un objeto Date según el valor proporcionado, en la hora UTC.
    - Date.prototype.setUTCHours(): Establece la hora de un objeto Date según el valor proporcionado, en la hora UTC.
    - Date.prototype.setUTCMilliseconds(): Establece los milisegundos de un objeto Date según el valor proporcionado, en la hora UTC.
    - Date.prototype.setUTCMinutes(): Establece los minutos de un objeto Date según el valor proporcionado, en la hora UTC.
    - Date.prototype.setUTCMonth(): Establece el mes de un objeto Date según el valor proporcionado, en la hora UTC.
    - Date.prototype.setUTCSeconds(): Establece los segundos de un objeto Date según el valor proporcionado, en la hora UTC.