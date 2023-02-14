# CSS
## Style inline
Es el responsable de todo lo visual de nuestra web.
Dentro de las etiquetas html, podemos agregar un ```style=""``` y agregar alfun estilo css...

## CSS en un archivo externo
Crear un archivo con extension .css y vincularlo al html.
**Vinculamos** => en el head => ```<link rel="stylesheet" href="estilos.css">```
El stylesheet hace referencia a un documento css.
Luego en el archivo .css puedo acceder a un elemento html, h1, p, table, etc abrir llaves y dar algun estilo.

## Declaracion de estilos CSS
Primero tomar un elemento HTML, para transformar/cambiar sus estilos (Lo malo de esto es que todos los elementos h1 por ejemplo, quedaran con esos estilos).
Segundo, definimos propiedades y valores.
```color: blue;```, las propiedades y valor estan siempre dentro de las llaves, color es propiedad, blue es valor.
**OJO en el orden en que se requieren los estilos, el ultimo en leer es el que se imprime.** => **A eso se refiere con estilos en cascada**

## Tres alternativas para trabajar con css
Podemos hacer un archivo aparte y luego vincularlo, para aplicar estilos al html.
Estilos en linea, son los que tienen mas jerarquia (estilos en cascadas), se aplican directamente en un etiqueta/elemento html, separado cada una de las propiedades dentro del estilem con ';', es como si style fuera el documento css.
**Usar etiqueta style dentro del head** => dentro de esta etiqueta resivo lo mismo que un archivo aparte. Selecciono elementos y les doy estilos.
**Lo mas recomendable es crear un archivo aparte, con la extension .css y vincularlo al html.**, separamos los archivos y el html queda mas limpio.
**Si se sobre-escriben los estilos, siempre prebalece el ultimo (estilos en linea.)**

## Colores: cuatro alternativas para sus valores
En el archivo css, puede llamar al color por su nombre, red, blue, green, peru... (El tema de los colores por nombre es que son limitados 140 aprox...)
Puede ser un color hexadecimal, #ffffff, #00ffcc, Red Grn Blue.
BackGroundColor, color de fondo.```background-color: pink;```
RGB y RGBA =>``` color: rgb(240, 100, 308); ``` ``` rgba(00, 50, 00, 0.7); ```, el ultimo numero en rgba hace alucion a la transparencia, va del 0, transparente, 1 sin transparencia.
Hay diferentes propiedades que tiene la posibilidad de agregar un valor de color.

## Tres formas de aplicar estilos en CSS (Etiquetas - ID - Classes)
Esto para aplicar estilos a las etiquetas de HTML...
Seleccionar un elemento de HTML en el CSS, esto seleccionara a todos esos elementos, ejemplo p{}, todo los parrafo quedaran con esos estilos **Esto es para estilos generales**.
**Los ids**, en html son unicos, no pueden haber de un elemento HTML con el mismo id. En el Html, en el elemento agrego id="nombreUnico" y en el CSS lo selecciono con #nombreUnico{} y agrego colores. El id no es muy usado en CSS ya que generalmente son unicos, y se pones mas de 1 puede causar problemas...
**Las clases** => son de los mas usando en CSS. en HTML lo declaramos como class="nombreClase" y en el CSS .nombreClase{}.
**# => id, . => clase, elemento HTML forma general**

## Comentarios
Con como los multiLine de Js, **/* */**.

## Buenas practicas
Siempre crear clases especificas para algo, para luego poder ir reutilizando, como las funciones...