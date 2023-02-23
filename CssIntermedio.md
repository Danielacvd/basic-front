# CSS Intermedio 2

## Border-style 
La idea es agregar bordes a la cajas, estos bordes tambien tienen muchos estilos...
En css, la propiedad es **border-style**, y puede tener de valor ser solid, dotted, double, inset, none, hidden, dashed.
Esto lo defino dentro de alguna clase y la agrego a algun elemento HTML.
The **border-style** property specifies what kind of border to display.
- dotted - Defines a dotted border
- dashed - Defines a dashed border
- solid - Defines a solid border
- double - Defines a double border
- groove - Defines a 3D grooved border. The effect depends on the border-color value
- ridge - Defines a 3D ridged border. The effect depends on the border-color value
- inset - Defines a 3D inset border. The effect depends on the border-color value
- outset - Defines a 3D outset border. The effect depends on the border-color value
- none - Defines no border
- hidden - Defines a hidden border

Los <p> tienen bordes, los div..., estas cajas tienen **ANCHO del 100% de lo disponible**, **elemento de bloque**
En cambios los <a>, su ancho se relaciona solo al numero de caracteres, no al **width** de la pagina, **elemento inline**


## Elementos de bloque y de linea
**Hay elementos que tienen el 100% del ancho disponible y otros solo usan un pedacito...**
**Esto es por la propiedad display**
Tenemos el **display: block** y **display: inline**...

**Elementos de bloque**, **TODOS ESTOS ELEMENTOS TIENEN UN SALTO DE LINEA**
- <div>
- <h1> - <h6>
- <p>
- <form>
- <encabezado>
- <footer>
- <sección>

**Elementos en linea**
- <span>
- <a>
- <img>

**Syntax**
**Propiedad =>** diaplay, **valor =>** block, **display: block**

**Estos son algunos de los estilos de los navegadores por defecto, establece el display-block a esos elementos de block, por DEFECTO**
**PARA CAMBIARLO**, si tengo una clase con **display: inline**, y se la **agrego a un elemento de bloque**, se comportara como elemento de linea, esto queiere decir que ya no usara el 100% del ancho disponible.
**Cuando a los elementos de bloque, le agrego estos display: inline, se van a ir acomodando uno al lado del otro, ya no uno debajo del otro..., ESTO SE DEBE A QUE HAY ESPACIO DISPONIBLE y son elementos de linea...**
**Tambien puedo transformar un elemento en linea a elemento de bloque**, a un <a> le creo una clase que tengo display: block, y se comportara de esa forma, usando el 100% del ancho disponible.



## Buenas practicas
Siempre crear clases especificas para algo, para luego poder ir reutilizando, como las funciones...
Siempre separar los estilos en diferentes clase, asi se le pueden aplicar a diferentes etiquetas. Siempre ir desde lo mas general a lo especifico. Lo doy estilos generales a los parrafos, pero a cada parrafo especifico le agrego sus estilos propios, ejemplo formateo los parrafos de una forma general, y cambio el color de cada uno. Estructurar los estilos, los colores juntos, los espaciados juntos...
**Buscar los estilos por defecto de cada navegador**
**Valores/Estilos por defecto de cada navegador [Link W3School](https://www.w3schools.com/cssref/css_default_values.asp)**
**Resetear los valores por defecto del navegador... se puede a mano o usando librerias (Normalize)**
**Todos los elementos HTML y sus atributos [Link htmlReference](https://htmlreference.io/)**