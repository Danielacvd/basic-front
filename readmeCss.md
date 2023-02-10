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
