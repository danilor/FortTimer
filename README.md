# FortTimer

**FortTimer** es un pequeño objeto de JavaScript que permite hacer cronómetros y conatdores de tiempo para páginas web. 

## ¿Otro cronómetro de tiempo?

La mayor diferencia de **FortTimer** con otros cronómetros que se encuentran en la Internet es su capacidad de mantener el conteo aún cuando el tab de un navegador no está siendo el foco de atención.

Por motivos de seguridad, en procesos controlados de intervalos de tiempo, la mayoría de navegadores bloquea estos procesos o los relentiza lo cual hace que, si un tab de un navegador no tiene el foco de atención, el contador no continúe o lo haga de manera muy lenta. Si por ejemplo un contador en una página tenía 30 segundos contados y se cambiaba de tab durante otros 30 segundos, al volver al tab original el contador podía llevar con mucho esfuerzo aún 31 segundos.

Debido a este problema, y a que no encontramos un contador de tiempo adecuado para nuestras necesidades específicas, se crea este contador de tiempo y cronómetro con la capacidad de continuar su cuenta aún si el navegador está realizando otras acciones o si el usuario tiene abiertos otros tabs del mismo.

## Requerimientos

* [Jquery 1.x +](https://jquery.com/)
* [JS Cookie](https://github.com/js-cookie/js-cookie)

## Ejemplos de uso

Es necesario incluir la librería junto a jQuery y la CookieJS si fuera a ser usada

```html
<script type="text/javascript" src="https://code.jquery.com/jquery-1.12.3.min.js"></script>
<script type="text/javascript" src="FortTimer.js"></script>
<script type="text/javascript" src="js.cookie.js"></script>
```

En la página es necesario colocar un **INPUT** que pueda contener los datos del contador.

```html
<p>
	<input type="text" value="00:00:00" id="timer" name="timer" />
</p>
```

### Funcionalidad básica

Y en el **document ready** de la página se inicia el contador

```javascript
FortTimer.element = '#timer'; // El elemento que va a contener el contador
FortTimer.cookie = false; // Si queremos cookies o no
FortTimer.logs = true; // Para efectos de desarrollo, si queremos mostrar todos los mensajes de consola
```

## Licencia

Este código está protegido bajo la [Licencia MIT](https://opensource.org/licenses/MIT).

