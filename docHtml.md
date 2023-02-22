# Basic Front, Html CSS BST5 Flexbox Sass...

## HTML
Conjunto de etiquetas para estructurar un sitio web, una maqueta, un esqueleto, luego con css trabajamos en la apariencia.
Se basa en etiquetas, que ayudan a que el contenido este estructurado dentro de un documento html.
**OJO** con los estilos del navegador por defecto, espaciado, tipografia, con css todo esto cambia, incluso algunos script de js, google fonts...

## Html5 etiquetas, estructura, ultima version estable
DOCTYPE!, solo le dice al browser que usamos html5
**Etiquetas con atributos?? implementado en html5???**
**html** => esta etiqueta, seria al contenido padre...engloba tanto el head, como el body, script...
**head** => encabezado, **informacion que le entregamos al navegador**, las etiquetas meta, generalmente no la ve el user?? solo el title, todo lo que esta dentro del head es info para el browser, info como palabras claves, descripcion de la web, titulo, estilos, scripts tambien...
**body** => es todo el contenido, todo lo que vera el user.

## Encabezados/Titulos y subtitulos
Desde el h1 al h6, varian en tamano, el 1 es mas grande y va a mas pequeno hasta el h6...

## Formato de textos
Las puedo ir mezclando todas en un parrafo, titulo, texto en general. Al igual que body y html, esta lleno de sub-etiquetas...
b => negritas (bold)
i => cursivas
s => para tachar texto
strong => le remarca, algo mas que las negritas, es para lo importante, que lo pinte como las negritas es cuestion del navegador.
del => para eliminar texto
ins => texto insertado (esta subrayado)
sub => tengo en subindice
sup => texto en super indice, es como el elevado en los numeros...
small => texto pequeno
mark => texto destacado, amarillo en google chrome.

## Listas o indices
ul => estructura de listas desordenadas
ol => estructura de listas ordenadas
li => item de la lista, la 'fila'

## Comentarios html
<!-- <li>Elemento</li> -->

## Vinculos, links
href toma el enlace para redireccion, ojo con las comillas, al igual que JS si abro con ` ' ", cierro con la misma comilla.
``` <a href="Esto es obligatorio"> Esto tambien </a> ```
``` <a href="pagina_2.html"> Pagina2 </a> ```

## Imagenes
Esta etiqueta no tiene cierre, ya que no pintamos contenido?? la img se pone ne le src, alt para mensaje cuando no se encuentra la imagen. **alt** es importante para el SEO
En src, pongo o el link de la imagen o la ruta donde se encuentra dentro del pc.
``` <img src="" alt=""> ```
Formatos de imagen soportada
JPEG
GIF, including animated GIFs
PNG
APNG
SVG
BMP
BMP ICO
PNG ICO

## Vinculos / Links con imagenes.
``` <a href="link"><img src="path img" alt="no hay foto"></a> ```

## Button
Etiqueta html5??

## Enlaces varios (emoticones para web...)
[Emojis](https://unicode-table.com/es/sets/top-emoji/)
[AtajosVscode](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)

## Tablas
Parte con ```<table></table>```, dentro van las filas y columnas
<tr> => fila (dentro de table) de la tabla, si agrego otro td en table, voy a tener la segunda fila...
<td> => columna (del de tr), es donde queda el contenido del tr (fila)
**border="1"** Atributo dentro de table, agrega los bordes da table...

## Tablas: Encabezados o Headers
<th> => Encabezado
Ahora en cada fila va el elemento correspondiente de cada encabezado.

## Tablas: Titulo o Caption
Se puede usar el h1 .. h6, pero tambien hay una etiqueta propia de las tablas para los titulos...
```<caption>Titulo</caption>``` Va dentro de <table></table> y queda centrado encima de la tabla. Siempre quedara encima de la tabla, aunque la definamos al final. El navegador establece ese orden.

## Tablas: thead, tbody, tfoot.
Si tenemos muchos tr, puede que el th se nos pierda.
La tabla se puede estructurar en diferentes secciones
```<thead></thead>``` => Para el encabezado, le agregamos el tr que contiene los th.
```<tbody></tbody>``` => aqui todo el contenido de la tabla. Todos los elementos tr...
```<tfoot></tfoot> =>``` se puede colocar donde se quiera, pero la recomendacion es despues del thead, es el mismo encabezado, pero para la parte inferior de la tabla. Es como para volver a poner el caption, pero en la parte del fondo, **recomendado para tablas extensas**

## Tablas: Combinar filas o columnas
Combinar celdas => se usa un td para cubrir 2 columnas, y al td se le agrega el atributo td ```colspan="AlgunNumero"```, el colspan toma el numero que le entregamos para combinar. Asi esa fila usa 2 columnas... **El segundo td, toma 2 colummnas para mostrar su contenido.**
**Tambien se pueden mezclar final** 
**```<br>```** => salto de linea en HTML
**```<br>```** => linea horizontal
**``` <td rowspan="3">Sin info</td> ```** => Ahora completara de forma vertical los campos que yo le indique, las filas que le indique.
Se puede mezclar horizontal **colspan** y veticalmente **rowspan**

## Formularios
Para que se ingresen datos y los procesemos, validemos si esta lleno, para esto Js, etc etc...
```<form></form>``` envuelve todo el formulario, el input, label, button...
Dentro del form podemos encontrar **action=""** que es un atributo que sirve para procesar el formulario...
```<input></input>``` Este input es la cajita donde se escribiran los datos del user... tiene un atributo **type=""** que es para agregar caracteristicas a los inputs (text, email, password...)(No tiene etiqueta de cierre), tambien puedo agregar un atributo **placeholder="Escribe aca"**, es una ayuda para la cajita, cuando se escribe en el input la ayuda se quita, atributo **id="nombre"** para relacionarlo con el label...
```<button></button>``` Para procesar ese formulario... y como es un boton dentro de un form, le agregamos ```type="submit"```, este tipo le dice al boton que va a procesar ese form. (preventDefault...)
```<label></label>``` es la etiqueta para relacionar, poner un texto de ayuda para los inputs, es opcional. Cuando se procesa el DOM es util. Relacionamos el texto con la cajita con el atributo **for="nombre"** que recibo el 'id' del input, tiene que ser el mismo que se use en el atributo del input id='nombre', **asi quedan relacionados el input con el label**.

## Formularios: Enviando Informacion
Si quiero recibir lo que se escribio en el input, tengo que agregar el atributo **name="nombreAqui"**, para asi relacionarlo con un nombre especifico. Ahora **nombreAqui** va a tener asociado el valor que se ingrese al input. Casi como una variable. Input puede resibir un name.
El **action=""** del form, es la accion del formulario, cada vez que se presiona el boton, se ejecutara action.La accion nos dice cual sera el destino de los datos de los inputs y a **name=""** le asociamos el valor que ingresa el user.
```<form action="enviando.html">``` cuando hago click en el boton me redirige y en la **URL** va lo que escribi en los inputs...

## Inputs: text, email, password, textarea, radio
En los inputs hay varios ***type=""**, text, email, password, textarea(que es mas grande que text), radio...
A los inputs se le puede agregar el atributo **required**, que es una validacion extra...
Password oculta la info, los caracteres.
**textArea** no va dentro de un input
``` <textarea name="" id="" cols="30" rows="10"></textarea> ```, el tamano predeterminado lo asigna las ```cols``` y ```rows```.
**Radio** es como un checkBox, es como para seleccionar el label haciendo click en el circulo, alternativas?, ademas tenemos que entregar el ```value="gato"```, que es lo que enviaremos al server cuando se procese el form.


## Inputs: color, date, file, month, range, time, week
Dentro del input, en el type tambien se le puede asignar tipo button, de esta forma ```<input type="button" name="" id="" value="Enviar">```, tambien hay type color ```<input type="color" name="" id="" value="Enviar">```
**type="date"**, y vemos un calendario
**type="file"**, y vemos una caja para seleccionar un archivo.
**type="month"**, y vemos un calendario de solo meses
**type="range"**, y vemos una linea para seleccionar un numero del 1 al 100
**type="time"**, y vemos reloj para seleccionar la hora. Por defecto es la del navegador en ese segundo.
**type="week"**, y podemos seleccionar la semana del anio!



### Test

