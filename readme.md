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