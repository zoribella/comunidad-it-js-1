# CSS - Cascade Style Sheet

## ¿Qué es CSS y para qué sirve?

**CSS** significa **C**ascade **S**tyle **S**heet o hoja de estilo en cascada y nos permite crear reglas que definen propiedades visuales para nuestros elementos.

**Ejemplo de código CSS:**
```CSS

span {
  color: white;
}

```

* En el código de ejemplo definimos que todos los elementos span de nuestro documento/s deben tener la tipografía de color blanco.
* De esta definifición vemos que tenemos una forma de seleccionar elementos y que podemos aplicar una propiedad para modificar la forma en que se ve el contenido de la etiqueta seleccionada.

**Ejemplo de código CSS:**
```CSS

selector {
  nombrepropiedad: valor;
}
```

* En CSS todo el tiempo vamos a estar utilizando estos dos conceptos: 
  * Seleccionar elementos
  * Definir como queremos que se vean
* Según como utilizemos CSS podemos definir como se ve un elemento, un documento o todo nuestro sitio


**IMPORTANTE**
* Una herramienta muy útil a la hora de trabajar con CSS y JavaScript es la [Devtools de Chrome](https://developers.google.com/web/tools/chrome-devtools)





## ¿Cómo seleccionar elementos y definir el color de texto?

### Color de texto
* Por medio de la propiedad **color** podemos establecer el color de tipografía que tiene un elemento
* Esta propiedad **color** acepta un color como valor, dentro de las opciones puede ser:
  * Nombre de color en ingles (white, red, blue, yellow, gray, etc)
  * Color en formato RGB (rgb(0,0,0)) donde cada valor va de 0 a 255 siendo 0 el apagado y 255 prendido
  * [Color Hexadecimal](http://www.blogoff.es/2008/11/19/colores-en-hexadecimal-una-introduccion/)
* Para saber más pueden visitar el [sitio de MDN](https://developer.chrome.com/devtools/docs/elements-styles)

### Selector básico por tipo de elemento
* Utilizando el selector por tipo de elemento podemos agrupar la forma de aplicar estilos a los elementos según el nombre de su etiqueta
* Este es un selector general ya que va a seleccionar **TODOS** los elementos del mismo tipo

**Ejemplo:**
```css
  p {
    color: blue;
  }

  div {
    color: rgb(255, 0, 0);
  }

  span {
    color: #00FF00;
  }
```

```html
<p>Texto en color azul</p>
<p>Texto en color azul y <span>verde</span></p>
<div>Texto en color rojo</div>
<div>Texto en color rojo y <span>verde</span></div>
<span>Texto en color verde</span>
```










## Colores
* Los colores en las computadoras están compuestos por 3 colores básicos llamados RGB que vienen de **R**ed, **G**reen y **B**lue, es decir Rojo, Verde y Azul
* Los monitores estan compuestos de píxeles que son como pequeñas lucecitas que pueden mostrar estos colores
* Cuando la luz esta **apagada** obtenemos el color **negro**
* Cuando la luz está en su **máxima intensidad en todos los colores** obtenemos el color **blanco**
* Existen diferentes sistemas para especificar un color:
  * Colores por nombre
  * RGB
  * HEXA
  * HUE

![Colores](../assets/css/rgb_model.gif)

### Nombre de color
* Existen nombres de colores que podemos utilizar directamente y el browser sabe como mostrarlos
* La lista de colores que podemos utilizar no es muy extensa por lo cual nos limita a la hora de elegir un color
* El nombre del color es en inglés (ejemplo: white/blanco)
* Son fáciles de utilizar
* En cada nueva versión de CSS se agregan más colores
* Ejemplos de colores: **white, silver, gray, black, red, blue, green, orange, pink, brown and yellow**

**Ejemplo:**
```css
body { color: black; }

p { color: gray; }

a { color: orange; }
```

[Lista de colores según versión de CSS](https://developer.mozilla.org/es/docs/Web/CSS/color_value)

### RGB
* Para este color utilizamos la función de CSS llamada **rgb**
* Podemos asignar un valor entre 0 y 255 a cada color
* Si todos los valores son 0 obtenemos el color negro
* Si todos los valores son 255 obtenemos el color blanco
* El orden de los colores es el especificado en el nombre, es decir que el primer valor es para rojo, el segundo para verde y el tercero para azul
* Ejemplos:
  * rojo: rgb(255, 0, 0)
  * verde: rgb(0, 255, 0)
  * azul: rgb(0, 0, 255)

**Ejemplo:**
```css
body {
  /* color negro */
  color: rgb(0, 0, 0);
}

p {
  /* color verde */
  color: rgb(0, 255, 0);
}
```

* Existe otra forma de utilizar rgb en CSS y es por medio de la función rgba() que agrega un canal más de transparencia
* Podemos asignar un valor entre 0 y 1 para el nivel de transparencia
* Se asigna como cuarto parámetro de la función

**Ejemplo:**
```css
body {
  /* color rojo */
  color: rgba(255, 0, 0, 1);
}

p {
  /* color rojo más transparente */
  color: rgba(255, 0, 0, 0.4);
}
```

### HEXA
* El sistema de HEXA representa los colores en Hexadecimal
* El color arranca con un numeral (#)
* Tenemos valores del 0 a la letra F
* Los números van del 0 al 9
* Continúan desde la letra A hasta la F
* Asignamos un par de letras para cada color del RGB
* Los dos primeros caracteres son para el rojo
* Los dos del medio son para el verde
* Los dos últimos son para el azul
* Si todos los valores son 0 tenemos el color negro (todo apagado)
* Si todos los valores son F tenemos el color blanco (todo prendido)
* Ejemplos:
  * blanco: #FFFFFF
  * negro: #000000
  * rojo: #FF0000
  * verde: #00FF00
  * azul: #0000FF

**Ejemplo:**
```css
body {
  color: #FFFFFF;
}

p {
  color: #FF0000;
}
```

* En caso de que las dos letras del mismo color se repitan podemos utilizar una sola, por ejemplo para blanco puede ser #FFF o negro #000

**Ejemplo:**
```css
body {
  color: #FFF;
}
```

### HSL
* Este sistema hace referencia a **H**ue, **S**aturation and **I**ntensity, es decir Matiz, Saturación e Intensidad
* Podemos establecer un valor entre 0 y 360 para el HUE según el color que queremos
![HUE](../assets/css/hue.png)
* Tanto saturación como intensidad aceptan un valor que va de 0 a 100%
* Ejemplo: 
  * negro: hsl(0, 0%, 0%)
  * blanco: hsl(0, 0%, 100%)
  * rojo: hsl(0, 100%, 50%)

[Calculador de HSL](https://www.w3schools.com/colors/colors_hsl.asp)
[Más sobre HUE)](https://es.wikipedia.org/wiki/Tono_(color))
[Más sobre HSL](https://es.wikipedia.org/wiki/Modelo_de_color_HSL)
[Más sobre colores](https://desarrolloweb.com/articulos/1503.php)

* En este sistema también contramos la función con alpha que funciona de la misma manera que el rgba.
* El cuarto valor acepta un número entre 0 y 1 para el nivel de transparencia que queremos
* Ejemplo: gris con transparencia: hsla(0, 100%, 100%, 0.5);}















## ¿Cómo agregar CSS?
* Existen diferentes formas de aplicar CSS
  * Se puede aplicar a nivel elemento utilizando el atributo **style** de HTML
  * En un documento por medio de la etiqueta **style** en el head
  * Compartido entre varios documentos utilizando la etiqueta **link** en el head de nuestros documentos que queremos vincular

### Agregar hoja de estilo en un elemento (atributo style)
* La forma más particular e individual que tenemos de utilizar css es utilizando el atributo **style** que tienen los elementos HTML
* Dentro del atributo style escribimos las propiedades visuales separadas por punto y coma

**Ejemplo:**
```html
<span style="color: white;">Texto en color blanco!!</span>
```

* De esta forma establecemos que **un** elemento span en particular va a tener el color de texto blanco
* Si quiero que **dos** o más elementos tengan el mismo color lo hacemos de la siguiente manera:

**Ejemplo:**
```html
<span style="color: white;">Texto en color blanco!!</span>
<span style="color: white;">Otro texto en color blanco!!</span>
```

* Geníal, ya tenemos 2 span con texto en blanco, ahora me pregunto, si tengo 50 span en el documento, los tengo que modificar uno a uno?, La respuesta es **NO** y ya vamos a ver cómo lo hacemos
* Cuando definimos estilos a nivel elementos lo estamos haciendo de forma individual
* Esta es una buena opción cuando necesitamos que si o si un elemento se vea de una determinada forma
* Utilizando esta definición de css se hace más difícil mantener o modificar nuestros elementos ya que para cambiar el color de una tipografía (como en el ejemplo) vamos a tener que modificar uno a uno todos los elementos (mucho trabajo)
* Si tenemos tan solo un documento puede ser una tarea relativamente simple pero si tenemos 300 documentos se hace más complicado
* Para evitar este problema necesitamos otra alternativa que nos permita definir los atributos visuales de nuestros elementos a nivel documento

#### Práctica
[Ejercicio 1](../ejercicios/consignas/css/ej1.md)

### Agregar hoja de estilo en un documento (style)
* Por medio de la etiqueta **style** podemos definir los estilos que queremos para nuestros elementos a nivel documento
* Utilizando selectores podemos cambiar la forma que se ve uno o muchos elementos del mismo tipo
* Para definir que el texto que estamos escribiendo dentro de la etiqueta **style** es css, utilizamos el atributo **type** con el valor "text/css"
* Si bien podemos omitir este atributo ya que HTML5 no lo require dejamos en manos del browser como interpretar el contenido de esta etiqueta
* Para estar más seguro y lograr mejor compatibilidad con browsers anteriores definimos el atributo **type** del elemento **style**

**Ejemplo:**
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Usando CSS</title>
    <style type="text/css">
      span {
        color: white;
      }
    </style>
  </head>
  <body>
    <span>Texto en color Blanco</span>
    <span>Texto en color Blanco</span>
    <span>Texto en color Blanco</span>
    <span>Texto en color Blanco</span>
    <span>Texto en color Blanco</span>
  </body>
</html>
```

* Con tan solo un cambio podemos establecer que todos nuestros elementos span se vean de otro color

**Ejemplo:**
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Usando CSS</title>
    <style type="text/css">
      span {
        color: red;
      }
    </style>
  </head>
  <body>
    <span>Texto en color Rojo</span>
    <span>Texto en color Rojo</span>
    <span>Texto en color Rojo</span>
    <span>Texto en color Rojo</span>
    <span>Texto en color Rojo</span>
  </body>
</html>
```

#### Práctica
[Ejercicio 2](../ejercicios/consignas/css/ej2.md)

* Esta forma de utilizar los estilos está buena cuando necesitamos definir estilos para un documento
* Si bien esta forma es más general que definir los estilos en cada elemento, sigue siendo una individual a nivel documento
* Un sitio va a tener más de un documento y si queremos mantenerlo necesitamos una forma de poder unificar todos los estilos para todos nuestros documentos

### Agregar hoja de estilo en un documento externo (link)
* Utilizando la etiqueta **link** podemos vincular un documento HTML con uno de CSS
* Todas las reglas que definamos en el documento CSS van a ser aplicadas en todos los documentos vinculados
* Esta es la mejor forma de unificar los estilos para nuestro sitio y es una forma más general de hacerlo
* La etiqueta **link** tiene los siguientes atributos y valores:
  * **href:** establece el path al documento CSS
  * **type:** al igual que en la definición de la etiqueta **style** especificamos que el contenido de este documento vinculado es "text/css"
  * **rel:** establece la relación con el otro documento y utilizamos el valor "stylesheet"

**Ejemplo:** 

Archivo: styles.css
```css
span {
  color: white
}
```

Archivo: index.html
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Index</title>
    <link href="styles.css" type="text/css" rel="stylesheet" />
  </head>
  <body>
    <span>Texto en color Blanco</span>
    <span>Texto en color Blanco</span>
    <span>Texto en color Blanco</span>
    <span>Texto en color Blanco</span>
    <span>Texto en color Blanco</span>
  </body>
</html>
```

Archivo: contact.html
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Contact</title>
    <link href="styles.css" type="text/css" rel="stylesheet" />
  </head>
  <body>
    <span>Texto en color Blanco</span>
    <span>Texto en color Blanco</span>
    <span>Texto en color Blanco</span>
    <span>Texto en color Blanco</span>
    <span>Texto en color Blanco</span>
  </body>
</html>
```

* Con tan solo un cambio en la hoja de estilo podemos modificar todos los documentos vinculados

**Ejemplo:** 

Archivo: styles.css
```css
span {
  color: red
}
```

Archivo: index.html
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Index</title>
    <link href="styles.css" type="text/css" rel="stylesheet" />
  </head>
  <body>
    <span>Texto en color Rojo</span>
    <span>Texto en color Rojo</span>
    <span>Texto en color Rojo</span>
    <span>Texto en color Rojo</span>
    <span>Texto en color Rojo</span>
  </body>
</html>
```

Archivo: contact.html
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Contact</title>
    <link href="styles.css" type="text/css" rel="stylesheet" />
  </head>
  <body>
    <span>Texto en color Rojo</span>
    <span>Texto en color Rojo</span>
    <span>Texto en color Rojo</span>
    <span>Texto en color Rojo</span>
    <span>Texto en color Rojo</span>
  </body>
</html>
```

#### Práctica
[Ejercicio 3](../ejercicios/consignas/css/ej3.md)

* CSS se llama Hoja de estilo en cascada ya que los elementos pueden **heredar** propiedades visuales de padre a hijo
* Si establecemos estilos al **body** todos los elementos que esten en el documento van a heredar esos atributos
* No todos los elementos son heredables
* Una buena forma de ver esto es utilizando la barra de [developer tools](https://developer.chrome.com/devtools/docs/elements-styles)
* Los estilos que definimos en un archivo externos pueden ser sobrescritos utilizando la etiqueta **styles**
* Los estilos definidos en style pueden ser sobrescritos utilizando el atributo **style** de los elementos
* De esta forma podemos ver que utilizamos conceptos generales y son pisados por los más individuales
* Este mismo concepto se da entre elementos
* Si definimos atributos visuales para el **body** podemos sobrescribir como se ven los **párrafos** por ejemplo dejando que el resto de los elementos hereden las propiedades declaradas en el **body**

**Ejemplo:** 

styles.css
```css
 p {
   color: red;
 }
```

```html
<link href="styles.css" type="text/css" rel="stylesheet" />

<style type="text/css">
  p {
    color: blue;
  }
</style>

<p style="color: black;">Texto en color negro!!</p>
```

* Como podemos ver en este ejemplo el estilo que establecemos en el elemento va a ser el que quede definido finalmente
* El estilo definido en el documento (etiqueta style) pisa el que esta definido en el archivo general. En este caso importa el orden en que fueron llamados los estilos
* Como regla podemos decir que siempre ponemos los estilos más generales primero y después sobrescribimos lo que necesitamos

#### Práctica
[Ejercicio 4](../ejercicios/consignas/css/ej4.md)








## Selectores
* Un selector es la forma en la que elegimos a que elementos queremos asignarle atributos visuales con CSS
* Los selectores pueden ser generales o particulares, es decír que puedo seleccionar varios elementos o tan solo uno y de forma muy particular
* Podemos utilizar un solo selector de la siguiente:

**Ejemplo:**
```css
selector {
  // código CSS
  // código CSS
  // código CSS
}
```

* Podemos utilizar más de un selector separados por coma:

**Ejemplo:**
```css
selector1, selector2 {
  // código CSS
  // código CSS
  // código CSS
}
```

### Tipo de etiqueta
* Es el selector que venimos utilizando en todos los ejemplos anteriores
* El selector por **tipo de etiqueta** nos permite elegir elementos por el **nombre de la etiqueta**
* Este tipo de selector retorna una colección de elementos ya que selecciona **todos** los elementos con el mismo nombre de etiqueta
* Por ejemplo podemos seleccionar los elementos p y h1 y definir que el color de texto sea blanco

**Ejemplo:**
```css
p {
  color: white;
}

h1 {
  color: white;
}
```

* Dado que ambos elementos se van a ver de la misma forma podemos escribir los selectores de la siguiente forma:

**Ejemplo:**
```css
p, h1 {
  color: white;
}
```

#### Práctica
[Ejercicio 5](../ejercicios/consignas/css/ej5.md)

### Selector universal
* Por medio del selector asterisco (*) podemos seleccionar todos los elementos
* Este selector se utiliza muchas veces para borrar estilos que vienen predefinidos en el browser

**Ejemplo:**
```css
* {
  color: white;
}
```

### Selector por clase
* Los elementos HTML tiene un atributo **class** que nos permite asignarles un nombre de clase
* En CSS podemos seleccionar los elementos por nombre de clase utilizando un punto y el nombre de la clase
* Este selector afecta a todos los elementos que tengan el nombre de clase seleccionado

**Ejemplo:**

En CSS:
```css
.rojo {
  color: red;
}
```

En HTML:
```html
<p class="rojo">Este texto es ROJO</p>
```

* Podemos hacer un selector más particular si queremos seleccionar sólo algunos elementos que tengan una determinada clase
* Si queremos seleccionar sólo los títulos H1 que tienen una clase rojo podemos hacerlo de la siguiente forma:

**Ejemplo:**

En CSS:
```css
h1.rojo {
  color: red;
}
```

En HTML:
```html
<h1 class="rojo">Este texto es ROJO</h1>
<p class"rojo">Este texto es NEGRO</p>
```

* Este último selector sólo selecciona los elementos del tipo h1 que tienen la clase rojo

### Selector por ID
* Los elementos HTML tienen un atributo ID que nos permite seleccionarlos de forma única
* Con CSS podemos seleccionar los elementos por ID utilizando el símbolo de numeral (#) y el nombre del ID del elemento
* Este es un selector individual ya que solo modifica un solo elemento
* Si queremos seleccionar el elemento que tiene el ID principial y establecer el texto en azul lo podemos hacer de la siguiente manera:

**Ejemplo:**

En CSS:
```css
#principal {
  color: blue;
}
```

En HTML:
```html
<div id="principal">Contenido de mi div en AZUL</div>
```

#### Práctica
[Ejercicio 6](../ejercicios/consignas/css/ej6.md)

## Hijos
* Podemos seleccionar los elementos que sólo son hijos directos de un elemento
* Utilizamos el símbolo mayor que (>) para elegir a a los hijos de un elemento

**Ejemplo:**
```css
div > p {
  color: red;
}
```
```html
<p>Texto de color negro</p>
<div>
  <p>Texto de color ROJO</p>
  <p>Texto de color ROJO</p>
  <h1>Texto de color negro</h1>
</div>
```

* En el ejemplo anterior vemos como podemos seleccionar sólo los párrafos que son hijos de un elemento div

#### Práctica
[Ejercicio 7](../ejercicios/consignas/css/ej7.md)

## Selector descendiente
* El selector descendiente permite seleccionar cualquier elemento

#### Práctica
[Ejercicio 8](../ejercicios/consignas/css/ej8.md)

* Ahora que sabemos varios selectores podemos ver más propiedades de CSS
* Existen más selectores y los vamos a seguir viendo más adelante

## Tipografías

### Familias
* Por medio de la propiedad **font-family** se puede establecer una lista de familias tipográficas
* Dado que todas las máquinas pueden no tener todas las tipografías instaladas podemos seleccionar más de una
* Las tipografías las separamos con comas. Ejemplo: Arial, serif
* El browser va a elegir cada tipografía de izquierda a derecha hasta encontrar una que tenga
* Los nombres de las tipografías se escriben con comillas dobles en caso de que el nombre contenga espacios, ejemplo: "Times New Roman", Georgia, serif
* Se recomienda poner una tipografía por default (serif, sans-serif, monospace, cursive o fantasy) para lograr al menos el estilo deseado
* También se pueden utilizar web fonts como pueden ser las de [Google](https://developers.google.com/fonts/docs/getting_started)
* Para saber más sobre la propiedad **font-family** pueden ver el [MDN](https://developer.mozilla.org/es/docs/Web/CSS/font-family)

**Ejemplos de tipografías por defecto**

![Fonts](../assets/css/fonts.png)

**Ejemplo:**
```css
body { 
  font-family: Arial, sans-serif; 
  color: black;
}

h1 {
  font-family: "Times New Roman", serif;
  color: gray;
}
```

* En este ejemplo definimos:
  * El texto del documento tiene que ser negro y con tipografía Arial o sans-serif
  * Los títulos h1 son grises y con tipografía Times New Roman o serif

### Tamaño
* Por medio de la propiedad **font-size** podemos establecer el tamaño de la tipografía
* Acepta como valor:
  * **Pixeles:** establecemos el número de píxeles y la palabra **px**
    * Es un valor fijo
    * Es ideal para pantallas de computadoras
    * No escalan bien para dispositivos mobile
    * No se pueden agrandar en browsers viejos
  * **Porcentaje:** es un % del valor establecido
    * Es relativo
    * Escala bien
    * Es fácil para cambiar la relación de todos los tamaños ya que definimos el valor inicial y después lo cambiamos en un solo lugar (el resto es todo relativo)
  * **EMS:** este valor representa una unidad del tamaño establecido
    * Si establecemos el tamaño a 10px, 1em representa 10px y 2em 20px
    * Si no se establece un valor toma el por default del browser (16px en general)
    * Se dice que toma el ancho y alto de la letra M
    * Es una unidad relativa al padre
    * Escala bien para mobile
    * Funciona en cascada
    * Un truco es establecer el tamaño del sitio en 62.5% tomando que el browser tiene 16px nos queda una tipografía inicial de 10px
    * Luego podemos utilizar valores como 1.8em para lograr una tipografía de 18px
  * **Points:** es una unidad para imprimir
    * 27 puntos representan una pulgada es decir 2,54 cm
    * Son precisos a la hora de imprimir
  * Para aprender más sobre el tema podemos seguir leyendo este buen artículo de [alistapart.com (en inglés y muy buen sitio)](https://alistapart.com/article/howtosizetextincss)
  * Una buena sección para mirar del mismo sitio: [Typography Web Fonts](https://alistapart.com/topic/typography-web-fonts)

  ![Font size](../assets/css/size.png)

  **Ejemplo:**
  ```css
  body { font-size: 100%; }

  p { font-size: 12px; }

  a { font-size: 1em; }
  ```

  ### Bold
  * Por medio de la propiedad **font-weight** podemos establecer si el peso de nuestra tipografía
  * Podemos establecer si es **normal** o **bold**
  * También acepta valores numéricos entre 100 y 900
  * Otra opción es utilizar valores relativos al padre por medio de **lighter** (más liviano) o **bolder** (más pesado)
  * Estas últimas opciones no son soportadas por todos los browsers
  * Podemos aprender más sobre esta propiedad en el [sitio de MDN](https://developer.mozilla.org/es/docs/Web/CSS/font-weight)

  **Ejemplo:**
  ```css
  .negrita { font-weight: bold; }

  h1 { font-weight: 900; }
  ```

  ```html
  <p>Texto en <span class="negrita">NEGRITA</span></p>
  <h1>Texto con negrita en 900 de peso</h1>
  ```

### Itálica
* Por medio de la propiedad font-style podemos establecer si queremos que nuestra tipografía sea normal, itálica o oblicua
* Los valores que acepta esta propiedad están en inglés:
  * nomral
  * italic
  * oblique
* Podemos aprender más sobre esta propiedad en el [sitio de MDN](https://developer.mozilla.org/es/docs/Web/CSS/font-style)

**Ejemplo:**
```css
.italica { font-style: italic; }

.oblicuo { font-style: oblique; }
```

```html
<p>Texto en <span class="italica">Italica</span></p>
<h1>Texto en <span class="oblicuo">Oblicuo</span></h1>
```

  ## Transformación de texto
  * Por medio de la propiedad **text-transform** podemos transformar las mayúsculas y minísculas de nuestros textos
  * A diferencia de lo que venimos viendo en este caso se utiliza text en lugar de font ya que hace referencia al texto y no a la tipografía
  * Acepta los siguientes valores:
    **uppercase:** pasa todo el texto a mayúscula 
    **lowercase:** pasa todo el texto a minúscula
    **capitalize:** convierte la primer letra de cada palabra a mayúscula
  * Podemos aprender más sobre esta propiedad en el [sitio de MDN](https://developer.mozilla.org/es/docs/Web/CSS/text-transform)

**Ejemplo:**
```css
h1 { text-transform: uppercase; }

p { text-transform: lowercase; }
```
```html
<h1>texto todo en mayúscula</h1>
<p>TEXTO TODO EN MINUSCULA</p>
```

### Alineado de textos
* Por medio de la propiedad text-align podemos establecer como queremos alinear los textos de forma horizontal
* Acepta los siguientes valores:
  * **left:** alinea todo a la izquierda
  * **right:** alinea todo a la derecha
  * **center:** alinea todo al centro
  * **justify:** hace que el texto ocupe toda la caja (justificado)
* Podemos aprender más sobre esta propiedad en el [sitio de MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)

### Decorado
* Por medio de la propiedad text-decoration establecemos si queremos decorar nuestras tipografía según los valores posibles:
  * **none:** saca todo tipo de decorado (es útil para hacer que los hipervinculos no tengan una raya debajo del texto)
  * **underline:** nos muestra el texto subrayado
  * **overline:**  agrega una línea sobre el texto
  * **line-through:** el texto aparece tachado con una línea en el medio (es útil a la hora de tachar elementos de una lista)
  * **blink:** Volvemos a los 90's y nuestros textos parpadean
* Podemos aprender más sobre esta propiedad en el [sitio de MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)

```css
a { text-decoration: none; }
h1 { text-decoration: underline; }
```

* En browsers más nuevo se puede establecer el color y tipo de línea que utilizamos
* Esta opción todavía [no es soportada por todos los browsers](http://caniuse.com/#search=text-decoration-color)
  * Primer parámetro el tipo de decorado
  * Segundo parámetro el tipo de línea (más sobre esto cuando vemos bordes)
  * Finalmente establecemos el color de la línea

```css
h1 {
  text-decoration: underline wavy red;
}
```

### Identación
* Podemos identar nuestro texto utilizando la propiedad **text-indent**
* Esta propiedad nos permite establecer un valor que va a funcionar como márgen izquierdo de la primer palabra de la primer línea.
* Acepta valores negativos
* Podemos aprender más sobre esta propiedad en el [sitio de MDN](https://developer.mozilla.org/es/docs/Web/CSS/text-indent)

**Ejemplo:**
```css
p { text-indent: 20px; }
```

### Sombra
* Para establecer la sombra de nuestro texto utilizamos la propiedad **text-shadow**
* Esta propiedad utiliza varios valores:
  * El primer parámetro maneja el eje x de nuestra sombra, es decir que va de izquierda a derecha
  * El segundo parámetro maneja el eje, es decir que va de arriba a abajo
  * El tercer parámetro maneja el blur (difuminar) de la sombra
  * El cuarto parámetro es el color de la sombra
* Podemos aprender más sobre esta propiedad en el [sitio de MDN](https://developer.mozilla.org/es/docs/Web/CSS/text-shadow)
* Los browsers actuales [soportan bien esta propiedad](http://caniuse.com/#search=text-shadow)

**Ejemplo:**
```css
p { text-shadow: 4px 2px 0px #000000; }
```

* Para jugar con estas opciones podemos usar el [siguiente sitio](http://www.cssportal.com/css3-text-shadow-generator)

### Espaciado o aire
* Podemos establecer la distancia tanto entre letras como palabras
* Para manejar la distancia entre letras utilizamos **letter-spacing**
* Para manejar la distancia entre letras utilizamos **word-spacing**
* Podemos aprender más sobre esta propiedad en el sitio de MDN:
  * [letter-spacing](https://developer.mozilla.org/en-US/docs/Web/CSS/letter-spacing)
  * [word-spacing](https://developer.mozilla.org/en-US/docs/Web/CSS/word-spacing)

```css
body {
  letter-spacing: 1px;
}

p {
  word-spacing: 2px;
}
```

### Alto de línea
* Podemos establecer el alto de línea de un texto por medio de la propiedad **line-height**
* Acepta un valor numérico
* Podemos aprender más sobre esta propiedad en el [sitio de MDN](https://developer.mozilla.org/es/docs/Web/CSS/line-height)

**Ejemplo:**
```css
p { 
  font-size: 12px;
  line-height: 18px;
}
```

### Alineado Vertical
* Podemos alinear los textos de forma verticual utilizando la propiedad **vertical-align**
* Acepta los siguientes valores:
  * baseline
  * sub
  * super
  * top
  * text-top
  * middle
  * bottom
  * text-bottom
* Algo común es creer que esta propiedad nos permite alinear los textos de forma vertical en los elemntos en bloque pero no funciona de esa forma
* Esta propiedad nos permite alinear el contenido de los elementos en línea
* Cómo sabemos las imágenes son elementos en línea al igual que los spans, hipervínculos, etc
* Si dentro de un párrafo tenemos una imágen, texto y otros elementos en linea, podemos establecer como va a ser la relación entre todos estos elementos que son hijos del párrafo
* De esta forma podemos hacer que un texto este bien alineado a una foto
* Un buen sitio para leer sobre este tema es [css tricks (en inglés)](https://css-tricks.com/what-is-vertical-align)

```css
img { vertical-align: bottom; }
```

## Modelo de Caja
* Podemos pensar los elementos de HTML como una caja
* Este concepto se conoce como box model

![Box Model](../assets/css/css-box-model.png)

* **content:** es el contenido del elemento, por ejemplo un texto u otros elementos
* **padding:** es un margen interno entre el borde y el contenido, podemos establecer diferentes valores para la parte superior, inferior, izquierda y derecha
* **border:** es el borde de la caja y se le pueden aplicar diferentes estilo
* **margin:** es el margen externo de la caja, podemos establecer diferentes valores para la parte superior, inferior, izquierda y derecha

* En HTML existen elementos del tipo en bloque (block) y en linea (inline)
* Estos tipos de elementos se diferencian en la forma que se comportan y como se aplican los atributos de la caja
* Los elementos en linea por ejemplo ignoran los márgenes superiror e inferior pero si aplica los de izquierda y derecha
* También los elementos en linea ignoran las propiedades de ancho y alto (lo vemos más adelante)

**IMPORTANTE**
* Para calcular el ancho de un elemento tenemos que tener en cuenta:
  * Ancho del elemento
  * Espacio asignado para padding (margen interno)
  * Ancho del borde
  * Espacio asignado a los márgines 
* Sumando todos estos valores obtenemos el ancho real de los elementos
* Algunos browsers viejos manejaban el modelo de la caja de otra forma y esto traía inconpatibilidad entre ellos