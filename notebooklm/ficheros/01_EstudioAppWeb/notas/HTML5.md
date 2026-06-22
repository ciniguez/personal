Para definir una página en HTML5, la siguiente sentencia debe estar en la cabecera del documento. Esta sentencia es una versión simplificada de la larga cabecera que se tenía en versiones de HTML anteriores a la versión 5.
```
<!DOCTYPE html>
```

## Estructura semántica
HTML 5 brinda etiquetas para estructurar el contenido considerando la semántica de las partes del documento. Similar a una revista o prensa escrita, un documento en HTML podría contener una cabecera, una barra de navegación, secciones de contenidos y artículos dentro de estas secciones. HTML 5 provee las siguientes etiquetas que permiten estructurar el contenido del documento considerando las diferentes secciones que podrían existir.
```
<article>
<aside>
<figcaption>
<figure>
<footer>
<header>
<hgroup>
<mark>
<nav>
<section>
<time>
<keygen>
<meter>
<summary>
```
## Controles de formulario
En HTML 5, el control **input** ha sido mejorado con interacciones para mejorar la experiencia de usuario y facilitar la validación de los datos ingresados por el usuario. Así, HTML 5 provee varias derivaciones del control input a través de atributos como son:
### placeholder
Proporciona sugerencias o ejemplo del contenido a ingresar por el usuario
```
<input type="text" placeholder="Ingrese su nombre">
```
### required
Entrada de usuario obligatoria
```
<input type="text" id="username" name="username" required>
```
Nota: required o required="required" son correspondientes
### autofocus
Enfocar en el control al cargar la página
```
<input name="q" autofocus />
```
### form
Si por un lado se tiene  formulario y por otro un control **button** o **submit** fuera del formulario. El atributo **form** es aplicado al control para indicar que al pulsar, se envíe el formulario (aun cuando el control no está dentro del formulario) [1].
```
<form id="myForm">
Add your telephone: <input type="tel" name="phone" required /><br />
</form>

<input type="submit" form="myForm" />
```
### autocomplete
Permite especificar si el agente (browser) tiene permiso para permitir el autollenado de los valores de los campos de formulario. Aplicable a controles: input (con entrada numérica o texto), textarea, select, form
```
<input name="lastName" id="lastName" type="text" autocomplete="family-name" />
```
En este contexto, también es factible utilizar un control **data-list** para conectar valores a un control input [2]
```
<label for="browser">Choose your browser from the list:</label>  
<input list="browsers" name="browser" id="browser">  
  
<datalist id="browsers">  
  <option value="Edge">  
  <option value="Firefox">  
  <option value="Chrome">  
  <option value="Opera">  
  <option value="Safari">  
</datalist>
```
### pattern
Permite indicar la expresión regular que validará la entrada del usuario.
```
Introduce tu TELEFONO con los 9 dígitos: <input type="tel" name="telefono" pattern="[0-9]{9}" title="El número ingresado no cumple con el formato">
```
### min, max
Permite establecer un rango de valores permitidos. Se puede aplicar en controles tipo number, range, date, datetime-local, month, time y week [3]
```
<input type="number" id="quantity" name="quantity" min="1" max="5">
```
### type="date"
Provee un control que permite al usuario ingresar una fecha. Soporta año, mes y día, mas no el tiempo. El tiempo es soportado por controles cuyo valor del atributo type es **time** y **datatime-local** [4]. Otros controles relacionados a fecha y tiempo son: **month** y **week**
```
<input type="date" id="start" name="trip-start" value="2018-07-22" min="2018-01-01" max="2018-12-31" />
```
### type="range"
Permite al usuario indicar un número dentro de un rango especificado [5].
```
<input type="range" id="volume" name="volume" min="0" max="11" step="1" value="3"/>
```
### type="color"
Permite al usuario especificar un color utilizando un selector de colores.
```
<input type="color" id="head" name="head" value="#e66465" />
```
### \<progress>
Etiqueta de HTML 5 que provee una barra de progreso [6]
```
<progress id="file" value="32" max="100"> 32% </progress>
```

## Referencias
1.- Cravens, J., & Burtoft, J. (2012). _HTML5 Hacks: Tips & Tools for Creating Interactive Web Applications_. " O'Reilly Media, Inc.".
2.- https://www.w3schools.com/tags/tag_datalist.asp
3.- https://www.w3schools.com/tags/att_input_min.asp
4.- https://developer.mozilla.org/es/docs/Web/HTML/Element/input/date
5.- https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/range
6.- https://www.w3schools.com/tags/tag_progress.asp