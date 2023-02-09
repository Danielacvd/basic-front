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

## Imagenes
Esta etiqueta no tiene cierre, ya que no pintamos contenido?? la img se pone ne le src, alt para mensaje cuando no se encuentra la imagen. **alt** es importante para el SEO
En src, pongo o el link de la imagen o la ruta donde se encuentra dentro del pc.
``` <img src="" alt=""> ```