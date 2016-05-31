# CSS

CSS significa hoja de estilos en cascada y sirve para darle estilo y formato a la estructura de un proyecto escrito en un lenguaje de marcado, ejemplo: HTML.

## Tabla de contenido

- Propiedades en CSS
 - [Over flow](#propiedad-overflow).
 - [Border radius](#propiedad-border-radius).
 - [Float](#propiedad-float).
 - [Display](#propiedad-display).
 - [Position](#propiedad-position).
 - [Box shadown](#propiedad-boxshadown).
 - [Min y Max](#propiedades-min-o-max).
 - [@Font face](#propiedad-font-face).
 - [@viewport](#propiedad-viewport).
 - [Clear](#propiedad-clear).
 - [Transformaciones](#transformaciones).
  - [función rotate()](#funcion-rotate).
  - [función translate()](#funcion-translate).
- [Pseudo elementos](#pseudo-elementos-en-css).
 - [first-child](#first-child).
 - [last-child](#last-child).
 - [nth-child](#nth-child).
 - [after](#after).
 - [before](#before).
- [Valores de herencia](#valores-de-herencia).
 - [Inherit](#inherit).
 - [Initial](#initial).
 - [Unset](#unset).
- [Referencias](#referencias).
- [FAQs](#faqs).
	- [Que es mobile first](#que-es-mobile-first)
	- [Que es un diseño elástico](#que-es-un-dise%C3%B1o-el%C3%A1stico)
	- [Que es responsive design](#que-es-responsive-design)
	- [Que es retina display](#que-es-retina-display)
	- [Que tipos de estilos existen en CSS](#que-tipo-de-estilos-existen-en-css)
	- [Como hacer que las fuentes se vean bien en todos los dispositivos](#como-hacer-que-las-fuentes-se-vean-bien-en-cualquier-dispositivo)
	- [Que son los colores hexadecimales](#que-son-los-colores-hexadecimales)
	- [Que significa el valor EM en CSS](#que-significa-el-valor-em-en-css)
	- [Que significa minificar un archivo en CSS](#que-significar-minificar-un-archivo-en-css)
	- [Que son los prefijos](#que-son-los-prefijos)
	
## Propiedad Overflow

Permite que se recorte el contenido de una capa, para mostrar únicamente el contenido que quepa, según sus dimensiones.

**Sintaxis**:

```css

#objeto 
{
	overflow: hidden|visible|auto|scroll;
}

```

**Valores**:

visible: Muestra todo el contenido de la capa así no quepa en ella.

hidden: Para ocultar el contenido que sobrepasa el alto y ancho que tiene asignado la capa.

auto: Muestra un scroll en la capa para poder mostrar contenido que sea mayor al tamaño de dicha capa.

scroll: Muestra un scroll en la capa así el contenido no sea mayor al tamaño de dicha capa.

**Gráficamente se vería así**:

![valores overflow](https://github.com/victorhtorres/ingenieria-informatica/blob/master/css/images/overflow-values.jpg?raw=true)


## Propiedad border radius

Permite darle estilos redondeados a las esquinas de las cajas. Esta propiedad nace en la versión CSS3.

**Sintaxis**:

```css

#objeto 
{
	border-radius: 1-4 length|% / 1-4 length|%|initial|inherit;
}

```
**Ejemplo 1**:

```css

border-radius:2em;

// is equivalent to:

border-top-left-radius:2em;
border-top-right-radius:2em;
border-bottom-right-radius:2em;
border-bottom-left-radius:2em;

```

**Ejemplo 2**:

```css

border-radius: 2em 1em 4em / 0.5em 3em;

// is equivalent to:

border-top-left-radius: 2em 0.5em;
border-top-right-radius: 1em 3em;
border-bottom-right-radius: 4em 0.5em;
border-bottom-left-radius: 1em 3em;

```

Los valores 0.5 y 3em del ejemplo 2, aproxima el grado de redondeo al eje x de la caja, ejemplo:

`border-top-left-radius: 10em;` produce lo siguiente:

![ejemplo border radius](https://github.com/victorhtorres/ingenieria-informatica/blob/master/css/images/border-radius-one-values.jpg?raw=true)

Ahora con dos valores:

`border-top-left-radius: 10em 5em;` produce lo siguiente:

![Ejemplo de border radius con dos valores](https://github.com/victorhtorres/ingenieria-informatica/blob/master/css/images/border-radius-two-values.jpg?raw=true)


## Propiedad float

Las propiedades display, float y position se usan de igual importancia en CSS3 y sirve para ajustar las cajas de información del sitio web. Con la propiedad float podemos colocar un objeto a la derecha o a la izquierda.

**Sintaxis*

```css
#objeto 
{
	float:left|right|intial|inherit;
}
```

>Elementos posicionados absolutamente ignora la propiedad float.

## Propiedad display

Display es la propiedad más importante para estructurar los objetos de nuestro sitio web. Cada elemento tiene un valor de display por defecto dependiendo de qué tipo de elemento sea. El valor por defecto para la mayoría de los elementos es usualmente block (de bloque) o inline (en línea). Un elemento que es block es comúnmente llamado elemento block-level. Un elemento inline siempre es llamado elemento inline.

**Sintaxis**

```css
#objeto
{
	display: block|inline|inline-block|none…;
}
```

**Tipos de display**

**Block**: `div` Es el elemento block-level estándar. Un elemento block-level comienza en una nueva línea y se estira hasta la derecha e izquierda tan lejos como pueda. Otros elementos block-level muy comunes son `p` y `form`, y algunos nuevos en HTML5 son `header`, `footer` y `section`.

**Inline**: El `span` es el elemento inline estándar. Un elemento inline puede contener algo de texto dentro de un párrafo `<span> como esto </span>` sin interrumpir el flujo del párrafo. El elemento `<a>` es el elemento inline más común, ya que se usa para links.

**Inline-block**: Permite tener varios bloques de elementos en una sola línea. Útil para la maquetación de la información.

**None**: Otro valor común de display es none. Algunos elementos especializados como script usan este por defecto. Es comúnmente usado en JavaScript para ocultar o mostrar elementos sin eliminarlos ni recrearlos. Esto es diferente de visibility. Usar `display: none` no dejará espacio donde el elemento se encontraba, pero `visibility: hidden;` dejará un espacio vacío.

**Descripción gráfica del display**:

![Decripción gráfica de la propiedad display](https://github.com/victorhtorres/ingenieria-informatica/blob/master/css/images/representacion-grafica-display.jpg?raw=true)

## Propiedad position

La propiedad position ofrece reglas alternativas para el posicionamiento de elementos.

**Sintaxis**

```css
#objeto
{
	position: static|absolute|fixed|relative|initial|inherit;
}
```

**Static**: Es el valor por defecto. Un elemento con `position: static;` no está posicionado en ninguna forma en específico y se ubicará según el flujo normal que tenga el HTML o en otras palabras, no tendra en cuenta los valores top, right, bottom y left que si aparecen con el atributo `position: relative;`.


**Relative**: Se comporta de la misma manera que static a menos que le agregues otras propiedades. La propiedad relative me genera 4 nuevos atributos: top, left, bottom, right.. Al darle valores a los nuevos atributos esto causará que la posición actual del objeto se reajuste.

**Fixed**: Un elemento fixed (fijo) se posiciona a la ventana del navegador de manera relativa, lo que significa que se mantendrá en el mismo lugar incluso después de hacer scroll en la página. Al igual que con relative, las propiedades top, right, bottom, y left también son usadas.

**Absolute**: Se comporta como fixed pero es relativo a su ancestro posicionado más cercano en lugar de ser relativo a la ventana del navegador, significa que, toma la posición (0,0) de la posición relativa más cercana. Si un elemento con `position: absolute;` no tiene ancestros posicionados, usará el elemento body del documento, y se seguirá moviendo al hacer scroll en la página. 

>Recuerda, un elemento "posicionado" es aquel cuyo valor es cualquiera excepto static.

## Propiedad box-shadown

Sirve para darle sombra a los elementos en CSS3.

**Sintaxis**

```css
#objeto
{
box-shadow: none|h-shadow v-shadow blur spread color |inset|initial|inherit;
}
```

Existe varias formas de representar sombras en los elementos por CSS3, por ejemplo:

**Ejemplo 1**:

```css
#objeto
{
	box-shadow: rgba(0,0,0,0.5) 5px 5px 20px
}
```

>Los primeros tres ceros del ejemplo hacen referencia al color en hexadecimal. El 0.5 hace referencia al % de transparencia (esto se debe a que el color RGBA añade un canal de transparencia). Los valores 5px 5px hacen referencia a los ejex (X,Y) y el valor 20px hace referencia al % de difuminación.


**Ejemplo 2**:

```css
#objeto
{
box-shadow: 10px 10px 5px #888888;
}
```

>Los dos valores de 10px del ejemplo 2 hace referencia a la posición de la sombra (se puede dar valores negativos para representar el otro lado del elemento a sombrear), el valor 5px hace referencia la longitud de radio de desenfoque de la sombra y el valor hexadecimal #888888 hace referencia al color de la sombra.


**Ejemplo 3**: Varias sombras.

```css
#bojeto
{
	box-shadow: 0 0 20px black, 0 10px 20px yellow;
}
```

>Puedo colocar varias sombras en un elemento con solo separar los valores por comas.

## Propiedades min o max

Es una propiedad adicional que se les puede dar a las otras propiedades como `width` y `height` y sirven para tener un límite de minimo o máximo de valor, dependiendo de la propiedad que uses.

**Sintaxis**

```css
#objeto
{
	min|max-height|width: valor;
}
```

## Propiedad @font-face

Sirve para especificar un tipo de fuente y la url donde se encuentra alojado el archivo. Ideal para utilizarlo con fuentes externas como las que ofrece el servicio [Google Fonts](https://www.google.com/fonts).

**Sintaxis**

```html
<!DOCTYPE html>
<html>
<head>
<style> 
@font-face {
    font-family: myFirstFont;
    src: url(sansation_light.woff);
}

@font-face {
    font-family: myFirstFont;
    src: url(sansation_bold.woff);
    font-weight: bold;
}

div {
    font-family: myFirstFont;
}
</style>
</head>
<body>
<div>With CSS3, websites can <b>finally</b> use fonts other than the pre-selected "web-safe" fonts.</div>
</body>
</html>
```
## Propiedad viewport

Sirve para controlar el comportamiento de la ventana de los dispositivos.

Sintaxis de ejemplo:

```css
@viewport
{
	width: 480px;
	zoom: 1;
}
```

## Pseudo elementos en CSS

Se utilizan para añadir efectos especiales a algunos selectores y/o etiquetas.

**Sintaxis**

```css
selector:pseudo-element 
{
	property:value;
}
```

También se puede poner selectores de clases e id's:

```css
selector.class:pseudo-element 
{
	property:value;
}
```

**Estos son algunos de los pseudo-elementos más utilizados**:


### first-child

La función first-child va a busca la primera etiqueta `<p>` que este dentro del objeto de nuestro interés y le agrega el estilo que definamos.

**Ejemplo**:

```css
footer p: first-child
{
	atributo: valor;
}
```

### last-child

Hará lo contrario a first-child, buscará el último `<p>` definido en el objeto para agregar algún estilo.

**Ejemplo**:

```css
footer p: last-child
{
	atributo: valor;
}
```

### nth-child

Atributo que sirve para darle estilo a una etiqueta `<p>` especifica de varias `<p>` que se encuentren en un contendedor. En otras palabras, si la caja de elementos tiene más de dos `<p>` se usa este atributo.

>Si no quieres complicarte con este atributo, simplemente usa un class para identificar la etiqueta la cual se desea darle estilo.

**Ejemplo**:

```css
p:nth-child(3)
{
	background:#ff0000;
}
```

### nth-child(odd)

Toma todos los elementos `<p>` pares de una caja.

**Ejemplo**:

```css
p:nth-child(odd)
{
	background:#ff0000;
}
```

### nth-child(even)

Toma todos los elementos `<p>` impares de una caja.

**Ejemplo**:

```css
p:nth-child(even)
{
	background:#ff0000;
}
```

### after

Inserta contenido después de un bloque `<p>`.

**Ejemplo 1**:

```css
p:after
{ 
	content:"- Remember this";
}
```

**Ejemplo 2**:

```css
footer p:last-child:after
{
	content: " -";
}
```

>En el ejemplo 2 vemos cómo se puede combinar dos pseudo-elementos. Tomará la última etiqueta `<p>` y le agregará después el " -".

### before

Inserta contenido antes de una etiqueta `<p>`

**Ejemplo 1**:

```css
p:before
{
	content:"Read this -";
}
```

**Ejemplo 2**:

```css
p:first-child:before
{
	content:"Read this -";
}
```
### Propiedad clear

Sirve para desplazar un objeto de otros que esten posicionados de manera flotante.

**Sintaxis**

```css
elemento {
    clear: /*right, left, o both*/
}
```

## Transformaciones

Nos permite hacer cambios a las características o a las propiedades de los elementos.

**Algunas funciones en las transformaciones**:

1. translate.
2. rotate.
3. scale.
4. skew.

**Sintaxis**:

```css

transform: funtion(valor);

```

## Funcion rotate

Para rotar los elementos.

**Sintaxis**:

```css

transform: rotate(valor);

```

**Unidades de medida en la función rotate**:


- deg: grados.
- grad: gradianes.
- rad: radianes.
- tunr: giros.

**Ejemplo**:

tomo el id de cualquier elemento del html y en css hago lo siguiente:

```css

#mifoto{
	transform: rotate(90deg);
}

```

## Funcion translate

Mover elementos de forma horizontal, vertical o las dos al tiempo.

**Sintaxis**:

```css

transform: translate(x,y);
transform: translateX(valor);
transform: translateY(valor); /* Al usarlo como translateCordenada(valor) tendra en cuenta el último. */

```

**Algunas unidades de medida**:

- px.
- em.

## Valores de herencia

Una de las características principales de CSS es la herencia de los estilos definidos para los elementos. Cuando se establece el valor de una propiedad CSS en un elemento, sus elementos descendientes heredan de forma automática el valor de esa propiedad.

A continuación, veremos algunos valores que permiten hacer herencia con base al valor que tenga sus elementos padres o valores predefinidos por los navegadores:

### inherit

Este es un valor que especifica que a la propiedad que se la apliquemos  debe de heredar los valores de su elemento padre. Podemos decir que la palabra Inherit significa  **Usa el valor de mi padre**, si el elemento padre no tiene definido dicho valor, el navegador seguirá el DOM hasta que encuentre un elemento superior que lo contenga, y en última instancia de no tenerlo ningún elemento superior, se aplicara el valor por defecto.

**Ejemplo**: Si tenemos el siguiente código HTML

```css
<div id="padre">
      <p>Hola soy el parrafo hijo del div con id padre</p>
</div>
```
y aplicamos el siguiente CSS:

```css
#padre {
     margin: 10px;
     border: 1px solid #000;
     color: blue;
}
#padre p{
     padding: inherit;
     border: inherit;
     color: inherit;
}
```

El elemento párrafo obtendrá el estilo del border y del color de su padre inmediato, que el `#padre` y el padding como no está definido en el padre inmediato, lo tomara de un elemento superior de acuerdo al árbol DOM.

### initial

Este valor pertenece a la especificación CSS3 y cuando aplicamos a una propiedad el valor initial estamos dando el valor inicial y predefinido por el navegador en cuestión. 

**Ejemplo**:

```css
body{
    font-size: 0.5em;
}
p{
    font-size: initial;
}
```

En este caso aunque tengamos un valor de tipografía definido para el cuerpo del documento, los párrafos tendrán un tamaño de fuente predefinida y por defecto, que general y normalmente es 1em, que por defecto es 16px.

>Los navegadores no tienen el mismo valor por defecto para ciertas propiedades.

### unset

Este valor unset es una combinación entre inherit e initial, cuando utilizamos este valor en una propiedad tratara de heredar el valor de su elemento padre si este está disponible, de no ser así este valor colocará el valor de la propiedad en su valor inicial, como si usáramos inherit e initial juntamente.

## Referencias

- [Desarrolloweb.com](http://www.desarrolloweb.com/articulos/atributo-overflow-css.html).
- [Learnlayout - Display](http://es.learnlayout.com/display.html).
- [Curso diseño web de Mejorandola](https://cursos.mejorando.la/diseno-web-online).
- [Learnlayout - Position](http://es.learnlayout.com/position.html).
- [W3schools - Ejemplos de positions](http://www.w3schools.com/cssref/playit.asp?filename=playcss_position).
- [Librosweb.es - Herencia](http://librosweb.es/css/capitulo_2/herencia.html).
- [Tutosytips - Valores de herencia en CSS3](http://www.tutosytips.com/valores-de-herencia-en-css3-con-inherit-initial-unset/#sthash.yVJmDxDG.dpuf).

## FAQs

### ¿Que es mobile first?

Es la nueva tendencia de empezar un proyecto en la web adaptada primero a dispositivos móviles e ir expandiéndose a resoluciones de pantalla mayores a 320px. Un ejemplo claro de esto es INSTRAGRAM, que empezó como app y terminó en escritorio. Se recomienda también poner un límite máximo del ancho en el diseño.

### ¿Que es un diseño elástico?

Es cuando el ancho de un proyecto web se adapta al tamaño de pantalla.

### ¿Que es responsive design?

Transforma el diseño para no mostrar ciertas partes o modificarlas con el fin de que respondan a la necesidad del diseño en otras resoluciones de pantalla.

### ¿Que es retina display?

Esto significa el doble pixeles por pulgada en las resoluciones de pantalla de los dispositivos móviles como iphone 4S+, Ipads tercera generación+, Android 4.0+ y entre otros... Esto es belleza pura para nuestros ojos pero sería una pena si tu diseño no está adaptado para retina display. La solución: exportar las imágenes de tu proyecto al doble de la resolución deseada. Ejemplo: un logo de 100px x 100px ahora debe ser a 200px x 200px. Las fuentes de nuestro sitio web no tendrán problemas en retina porque son vectoriales y se escalan matemáticamente. Para más información sobre retina display, puedes consultarlo el siguiente artículo en cristalab: http://www.cristalab.com/blog/que-significa-retina-display-en-el-diseno-web-c108299l/

### ¿Que tipo de estilos existen en CSS?

Existen tres tipos de estilos: Las etiquetas propias de HTML (header, setion, footer, etc..), ID´s (#nombred_del_div) y Clases (.estoesclase).

### ¿Como hacer que las fuentes se vean bien en cualquier dispositivo?

Las fuentes son vectoriales y no se pixelan como si es el caso de las imágenes (que no son vectoriales) a los cambios de resolución de pantalla, pero es recomendable usar como tamaño mínimo de 16px en los proyectos.

### Que son los colores hexadecimales?

La descripción RGB (del inglés Red, Green, Blue; "rojo, verde, azul") de un color hace referencia a su composición de la intensidad de los colores primarios con que se forma: el rojo, el verde y el azul. Por medio de la mezcla de intensidad de los tres colores, podremos representar muchos más. 

Para indicar con qué proporción se mezcla cada color, le asignamos un valor a cada uno de los colores primarios, así, por ejemplo, el valor 0 significa que no interviene en la mezcla, y en la medida que ese valor aumenta, aportará más intensidad a la mezcla. La gama de colores de la web consiste en 216 combinaciones de rojo, verde y azul, donde cada color puede tomar un valor entre seis diferentes (en hexadecimal): #00, #33, #66, #99, #CC o #FF, que tienen un porcentaje de intensidad de 0%, 20%, 40%, 60%, 80% y 100%, respectivamente.
Este sistema utiliza la combinación de tres códigos de dos dígitos para expresar las diferentes intensidades de los colores primarios RGB, por ejemplo:

Blanco y Negro

negro: #000000 donde los canales estan al minimo: 00, 00, 00.
blanco: #FFFFFF donde los canales estan al maximo FF, FF, FF.

### ¿Que significa el valor EM en CSS?

En algunos casos en vez de utilizar tamaños en px en fuentes, imágenes y padding, se puede usar em, que significa el tamaño de una "M" (la letra más cuadrada del abecedario) y CSS lo que hace es buscar el valor px más cercano y lo asume a 1em, ejemplo: Si le asignamos a una caja el tamaño de letra a 2em, entonces CSS buscará el valor más cercano en px en forma de cascada y encuentra uno por valor de 16px, entonces multiplicara 2x16 y el tamaño real de los 2em será 32px.

### ¿Que significar minificar un archivo en CSS?

Minificar el CSS en esencia consiste en eliminar todos los espacios en blanco que tenga dicho documento así como unificar clases o id’s los cuales tengan los mismos parámetros definidos. Gracias a esto podemos mejorar el tiempo de carga de nuestra web y por tanto el consumo de CPU de la misma. Fuente:  http://tecnodiseno.com/que-es-minificar-el-css-y-5-herramientas-online-para-realizarlo/

### ¿Que son los prefijos?

Los prefijos son modificadores que le anteponemos a las nuevas propiedades de css3 que no son muy bien interpretadas por los navegadores para que cada navegador por medio de este modificador haga que el navegador interprete este fragmento de código de CSS3. Estos son los prefijos de los principales Navegadores:

```plain
-moz-: (para navegadores basados en Gecko como Mozilla)
-webkit-: (para navegadores basados en Webkit, como Chrome o Safari).
-o-: (para Opera)
-ms-: (para internet explorer)
```
Solo se debe colocar cada prefijo antes de la propiedad css3 para que el respectivo navegador reconozca la propiedad y las características, ejemplo:

```css
#my-id 
{
     border-radius: 1em //propiedad estandar en CSS3.
    -moz-border-radius: 1em;
    -webkit-border-radius: 1em;
    -o-border-radius: 1em;
    -ms-border-radius: 1em;
    
}

```
