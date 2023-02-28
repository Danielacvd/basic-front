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

Los ```<p>``` tienen bordes, los div..., estas cajas tienen **ANCHO del 100% de lo disponible**, **elemento de bloque**
En cambios los ```<a>```, su ancho se relaciona solo al numero de caracteres, no al **width** de la pagina, **elemento inline**


## Elementos de bloque y de linea
**Hay elementos que tienen el 100% del ancho disponible y otros solo usan un pedacito... aca podemos distribuir el ancho y alto sin problemas**
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

**Elementos en linea, aqui no se permite establecer un ancho y alto.**
- <span>
- <a>
- <img>

**Syntax**
**Propiedad =>** diaplay, **valor =>** block, **display: block**

**Estos son algunos de los estilos de los navegadores por defecto, establece el display-block a esos elementos de block, por DEFECTO**
**PARA CAMBIARLO**, si tengo una clase con **display: inline**, y se la **agrego a un elemento de bloque**, se comportara como elemento de linea, esto queiere decir que ya no usara el 100% del ancho disponible.
**Cuando a los elementos de bloque, le agrego estos display: inline, se van a ir acomodando uno al lado del otro, ya no uno debajo del otro..., ESTO SE DEBE A QUE HAY ESPACIO DISPONIBLE y son elementos de linea...**
**Tambien puedo transformar un elemento en linea a elemento de bloque**, a un <a> le creo una clase que tengo display: block, y se comportara de esa forma, usando el 100% del ancho disponible.

## Padding
Con el padding, **generamos espacio/relleno alrededor del contenido HTML**.
Entonces tenemos una caja, un <div>, dentro un <p>, si al <p> le agrego un padding generare relleno, espacio entre el contenido y el borde. Tengo TOP BOTTOM LEFT RIGHT, que son la direccion, hacia donde quiero agregar el padding, **siguen el sentido del relog**, arriba derecha abajo izquierda.
**Si solo doy un padding: 100px**, tomara esos 100px en todos los ladtos, si solo tengo 2 valores, el primero toma arriba abajo y el segundo derecha izquierda.
**Ser siempre especifico ser mas declarativo, se ve mas codigo, pero queda mucho mas claro que es lo que hace X clase**, si quiero padding hacia arriba padding-top: 10px, y lo mismo para las demas orientaciones.
**Siempre revisar en el inspector de elementos, el valor en pixeles, orientaciones, etc...**
**px => padding para eje x, derecha izquerda**
**py => padding para eje y, arriba abajo**
![Modelo de cajas!](/imgDocu/modelo-caja.png "Modelo de cajas")
![Modelo de cajas!](/imgDocu/modelo-cajas-2.png "Modelo de cajas")

## Margin
El padding era el relleno de la caja, luego viene el border y finalmente el margin, su margen, su usan para crear un espacio alrededor de los elemeentos, fuera de los bordes definidos...
Usamos **la propiedad margin** y los valores pueden ser top, bottom, right, left.

## Altura y ancho, height y width
Se usan para establecer el alto y ancho de un elemeneto, a un parrafo le agrego una clase border, en el css agrego en una clase width: 100px, height: 100px... Y esto establece el ancho y alto.

## Inline-block, ancho y alto para elementos en linea
Por defecto un ```<a>``` tiene un display inline, por lo que si quiero agregar un ancho a un ```<a>``` tengo que crear una nueva clase, en css creo la clase d-inline-block y le agrego **display: inline-block**, y ahora si puedo establecer ancho y alto para esos elementos, **ya no es inline, es inline-block**
**La diferencia entre inline-block y los elementos de bloques, como un parrafo, es que no agrega un salto de linea.**.
Y ahora los ```<a>``` se van a poder agregar uno al lado del otro **asi un ```<a>``` puede parecer un boton**

## Modelo de caja
**El modelo de cajas sirve para hacer calculos**, si quiero calcular el ancho total de una caja, tengo que conciderar el ancho, padding, border, margin..., por lo que, **aunque digamos que una caja es de 320px** al final sera de **350px**, por todo lo que se le agrega (a veces por defecto),
**Esto es un problema, si el ancho de pantalla es de 600px y quiero sacar ese calculo y saber cuantas cajas puedo poner horizontalmente tengo que tomar en concideracion esto**, establecer un ancho de la caja, pero tambien sumar el padding y border... **Para facilitar esto existe el box-sizing**
![Modelo de cajas w3](/imgDocu/modelo-caja-w3school.png "Modelo de cajas")

## Box-sizing: border-box, ajustes automaticos de anchos y altos
Para saber el ancho total de una caja, tengoq ue hacer muchas sumas... para facilitar esto box-sizing...
**box-sizing:** es una propiedad, y **border-box** que es su valor, soluciona el tema de los calculos de css.
En html inventamos la clase border-box, en css:
 ```
.boder-box{
    box-sizing: border-box;
}
```
Ahora en el elemento HTML, vemos como mantiene su ancho establecidom width: 100px, y lo respeta... lo revisamos en el inspector, el contenido, como el border como el padding **se esta ajustando, se apreta, se junta todo, para que el ancho no sea mayor a 100px...**, el margen queda fuera del calculo, ya que es exterior.
**Con esto no tenemos que realizar calculos, del padding izq con el derecho, no los border... siempre sera el ancho establecido...**

## Normalize CSS
Esto hace que todos los navegadores procesen los elementos de manera consistente. Lo que quiere decir que elimina los estilos/configuracion por defecto que tienen los navegadores.
Solo se tiene que descargar, esto nos da una hoja en css, en donde resetea los elementos HTML, y lo dejamos dentro de un documento css
[Normalize](https://necolas.github.io/normalize.css/)

## REM vs EM
### Diferencia entre unidades relativas y absolutas
**Medidas absolutas:** el valor se encuentra definido en terminos contretos y de manera medible, 100px, esto jamas cambiara, siempre seran lo mismo...
**Medidas relativas:** tienen relacion y se calculan a partir de otro valor de referencia... puedo usarlas en decimales, 0.5rem.
**Unidad Relativa 1:** REM, esta es relativa al HTML, especificamente al font-size, por defecto es de 16px, que es una medida estandar.
Cuando se habla de 1 rem, esto quiere decir que el 1 se multiplica por el tamano base, que es 16, 1*16 y esto serian 16px, 1rem = 16px, asi sucesivamente.
**Esto es independiente a los elementos anidados que pueda tener, siempre tomara los 16px del HTML**
**Unidad relativa 2:** EM, si pongo 0.5em, el resultado sera el mismo 8px, **la diferencia del em, es que no siempre va a tomar el HTML**, si yo especifico que el body **el contenedor padre** del h1 en donde estamos probando, si en el body pongo font-size: 32px, se nota un cambio, ya que **em** va a buscar el font-size del h1 y como no lo tiene establecido va a subir un nivel, al body, y el body tiene un font-size de 32px, por lo que esa sera su unidad base. **Esta es la principal diferencia.**
**El rem siempre independiente de su contenido supeior/padre TOMARA el del HTML.**
```
html{
    font-size: 16px;
}
body{
    font-size: 32px;
}
h1{
    font-size: 1rem;
}
```
**Esto no solo se usa para font-size, tambien para los padding**, padding: 1rem => 16px a todos lados...
**Cual es la gracia de usar em, ya que rem es mas sencillo de usar...** => 
**Esto lo puedo revisar en el inspector de elementos en COMPUTED** 

## Buenas practicas
Siempre crear clases especificas para algo, para luego poder ir reutilizando, como las funciones...
Siempre separar los estilos en diferentes clase, asi se le pueden aplicar a diferentes etiquetas. Siempre ir desde lo mas general a lo especifico. Lo doy estilos generales a los parrafos, pero a cada parrafo especifico le agrego sus estilos propios, ejemplo formateo los parrafos de una forma general, y cambio el color de cada uno. Estructurar los estilos, los colores juntos, los espaciados juntos...
**Buscar los estilos por defecto de cada navegador**
**Valores/Estilos por defecto de cada navegador [Link W3School](https://www.w3schools.com/cssref/css_default_values.asp)**
**Resetear los valores por defecto del navegador... se puede a mano o usando librerias (Normalize)**
**Todos los elementos HTML y sus atributos [Link htmlReference](https://htmlreference.io/)**
**font-size: 1rem;** siempre lo usan en rem, 16px el tamano del texto y 16 de padding, para que el font-size y el padding queden iguales, ya que el **em** toma la medida de su contenedor, para este caso el mismo H1, ya que queda establecido, toma la medida del H1... **Si aumento el tamano de la fuente, proporcionalmente aumenta el padding, esta es la gran ventaja, nos ahorramos configurar el padding, ya sabemos que si la fuente crece tambien lo hara el padding, para que nuestra caja siempre tenga ese crecimiento proporcional, entonces 1em siempre sera relativo al tamano de fuente, para este caso el h1 que esta tomando 2rem, que serian 32px de font-size...**, asi se cambian al valor del font-size a 3rem, no tengo que hacer tanto calculo para tener un buen padding y que crezca proporcionalmente, ya que el 1em esta tomando esa unidad relativa del font-size...
**Siempre que quiera que el contenido crezca proporcionalmente,  padding, margin, width, height usar em, para lo demas como los texto REM.**
![REM EM Unidades relativas](/imgDocu/emVSrem.png "Modelo de cajas")
[Google Fonts](https://fonts.google.com/), elijo la que me gusta, agrego los style y finalmente hago un link y lo llevo al head... y luego en el css, body, font-family que tambien lo saco de google.
