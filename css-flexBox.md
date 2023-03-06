# Resumen FlexBox

[GuiaFLexBox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
[Guia2FLexBox](https://cssreference.io/flexbox/)
[ConceptosBasicosFlexBox](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)

## Configuraciones Iniciales y Lore
FlexBox permite hacer distribuciones de nuestras cajas, los div...
Lo primero es en el body, le agregamos una clase container a body, para poder centralizar todo el contenido, las cajas quedaran dentro de este container.
A este container, en css, le agrego width 90%, lo centramos con margion left y right automatico... para centrarlo.
**Segundo**, dentro del container (el body), se crea un div, que tiene la clase border, y este div, va a tener adentro 3 div mas, queda uno tendra la clase item!... hacemos 3 y quedara una caja que contiene 3 cajas mas.
Agreegamos algunas clases a .item, un background-color, borders... 

## display: flex; (contenedor padre)
Ya tenemos un contenedor padre y elemenetos en su interior, el div con clase border que contiene 3 divs con clase items.
**El primer div, es el contenedor padre, ya que almacena a cada uno de sus hijos...**.
**En flex box es el contenedor padre es importante, por lo que veremos las propiedades del contenedor padre**
**Propiedades del contenedor padre, lo mas importante, de momeneto no se tocaran los items**
**Creamos una clase para el contenedor padre, flex-container**, este lo creamos en el css, ya sabemos de los diaplay inline y block, pero tambien esta el **display: flex**, le agregamos esta propiedad a la clase y vemos que cada item se puso uno al lado del otro, **ahora los elementos son flexibles**... **varias de las cosas que pasan en flexbox estan dadas por defecto**
**Ahora en contenedor padre tiene un display flex, asi sus elementos hijos se colocan uno al lado del otro.**, pero no quiere decir que sea un display inline, ahora son elementos flexibles

## flex-direction
Con esto puedo **distribuir cada una de las cajas hijas**, de izq a derecha, de derecha a izq, o en forma de columnas, de arriba abajo, abajo arriba... Estas propiedades y valores se establecen con **flex-direction**.
**En la misma clase del contenedor padre, agrego el flex-direction**, ya que flex-direction depende de display: flex... 
**flex-direction por DEFECTO estara en row**, por lo que van de izq a derecha, con el valor **row-reverse**, se distribuye de derecha a izq, **column** para que distribuya de arriba hacia abajo, **column-reverse** distribuye de abajo hacia arriba.
**flex-direction ayuda mucho para hacer web responsivas.**


## flex-wrap
En ninguno de los elementos, items, tenemos un ancho establecido. Si en item agregamos width:200px, cada caja va a tener 200px.
**Si achicamos la ventana cada caja se ira apretando, tanto que al final se desbordan de su contenedor y de la web**.
**flex-wrap, para configurar que tanto se iran achicando/apretando**.
En la clase flex-container, agregamos **flex-wrap: nowrap**, **nowrap** es el valor por defecto del flex-wrap **todos los elementos flexibles estaran en una sola linea**... asi que si vemos si algo cambia, no lo hara, se seguira achicando hasta salirse del contenedor padre.
**flex-wrap: wrap; nos asegura que cada uno de los item sera de 200px, lo que establecimos. Por lo que si otro elemento no cabe  va a pasar a la parte de abajo.** Asi flexbox nos asegura que si a un item le asignamos una X cantidad de ancho siempre se vera de ese ancho y si en donde esta contenido no alcanza un proximo elemento, este sera empujado abajo. **flex-wrap: wrap; respetara el ancho y nustras cajas no se apretaran... a menos que el sitio web se encoja mucho, en ese caso si se encojeran los items para que sigan cabiendo en la caja padre.**

## justify-content
Eso es para distribuir los items que tengo en el contenedor padre, **esta propiedad la agrego en la clase del contenedor padre**.
**justify-content: center**, cada uno de los elementos se posicionan en el centro del contenedor padre.
**justify-content: space-between**, una caja se posiciona a lo mas izq que puede, otra al centro y otra a lo mas derecha que puede.
**OJO que para todos estos ejemplos, estamos usando como contenedor padre el div, por lo que todos los items que agrego se van a gregando en una sola linea (si es que tengo la pantalla completa), si tubiera mas alto, intentarian abrir una segunda fila.**
**justify-content: space-around**, para agregar un espaciado al lado izq y derecho y entre medio de cada elemento.
**POR DEFECTO el justify-content: es flex-start**

## align-items
Para esto establecemos un alto para el contenedor padre. Con una clase le agrego una altura de 700px...
**Al hacer esto cada uno de los items, que no tienen un alto configurado, pero de todas formas como el contenedor padre tiene 700px, ellos tratan de abarcar el 100% hacia abajo. Esta es la propiedad que se llama align-items y por DEFECTO ESTA EN stretch, que trata de abarca el 100% hacia abajo**
**En el contenedor padre, agregamos align-items: flex-start**, los elementos se posicionan en la parte superior y **respetan su altura correspondiente**, con **flex-end** se posicionan en la parte inferior... **ESTOS EJEMPLOS se pueden realizar SIEMPRE QUE EL CONTENEDOR PADRE TENGA UNA ALTURA DEFINIDA.** **Si un elemento hijo tiene su altura definida, tambien se acomodara**, para esto usamos el **baseline**, que tratara de posicionar los elementos a partir de la base, como un texto.
**aling-items: center**, los elementos se posicionan al medio de la pantalla.

## align-content
Con esta propiedad podemos distribuir cada uno de los items, ya sea separandolos, dejandolos juntos al incio o al final, etc.
Es parecido al justify-content, solo este actua en forma horizontal y ahora trabajaremos de forma vertical...
**Para trabajar de forma vertical, al menos hay que tener 2 filas.**
**En el contenedor padre, agregamos align-content: space-between**, los elementos se ordenan hacia arriba y hacia abajo. **Esto va cambiando siempre y cuando tengamos mas de una fila, si todos los elementos estan en una fila no se notara.**
**Cuando se trabaja con mas de una fila se distribuiran de forma vertical**. **No es lo mismo que elign-items que funciona de forma horizontal, tomamamos toda la fila y la posicionamos en alguna altura del contenedor padre.**, **cuando tenemos mas de una fila, podemos cambiar esa distribucion con align-content**

## Hasta aca todo lo del contenedor padre... los elementos hijos tienen otra propiedades y valores.

## Desde aca, items hijos...

## order (elementos hijos)
Para modificar el orden en el que se visualizan los elementos, usamos el order.
**Esta propiedad no se agrega al contenedor padre, la configuramos por separado y luego se la agregamos al item**
**order-1{order: 1}**, si esto se lo agrego a un elemento lo mandara al final de la lista... ya que **con order establacemos la prioridad**, va desde el 0 al infinito... **por defecto esta configurado en 0, por lo que todos los elementos que tengan el order: 0, se posicionaran antes de los demas**, por lo que el 1, no es de tanto prioridad..., el 0 es la maximo prioridad... mientras mas bajo el numero del order mas a la izq, o primero aparecera el item. La prioridad de order es la que manda y se puede configurar. Va de 0 al infinito, el 0 es la mayor prioridad.

## flex-grow
(para visualizar bien, sacar el justify-content de la clase pabre, y sacar los oreders.)
Tambien sacamos el ancho de 200px, de cada item, **solo abarcaran segun el CONTENIDO que tenga cada item**, si a un item le agrego mas texto, este va a tener mas ancho, ya que el contenido necesita mas espacio...
**Con flex-grow, puedo distribuir y manejar esos espacios**, al igual que ```order``` creo la clase por separado para luego agregarla a los items, no la creo directo en el contenedor padre.
**A la clase, le damos el nombre flex-grow-1, agregamos la propiedad flex-grow: valor 1**, esta clase de la agrego a un elemento, **este elemento trata de abarcar el mayor espacio disponible, dejando a los otro elementos con su tamano por defecto**.
**Flex-grow ayuda con la distribucion de cada uno de los elementos**, si a todos los elementos les agrego el flex-grow: 1, cada elemento va a tratar de usar el mayor espacio disponible, aunque da el aspecto de que tratan de distribuir el espacio de forma igualitaria.
**Si a una clase le agrego flex-grow: 2 y lo agrego a un elemento, este, tratara de usar el doble de espacio de que usen los otros elementos**. **No es exactamente el doble que los otros lementos, pero trata de abarcarlo.**.
**Si a todos los elementos los tengo con flex-grow: 1, todos tienen la distribucion con el mismo tamano, y esto es lo bueno, ya que NO TENEMOS QUE ESTAR CALCULANDO EL ANCHO PARA CADA ELEMENTO HIJO.**

## flex-shrink
Hace que el item con esta clase **no se reduzca de su tamano establecido**.
Creamos la clase flex-shrink-0, y le damos la propiedad flex-shrink: 0, **si se la agregamos a algun elemento, ESTE YA TIENE QUE TENER ESTABLECIDO EL ANCHO MINIMO PARA FLEX-SHRINK**, por lo que cambiamos lo anterior y en la clase flex-shrink-0, agregamos width: 300px; flex-shrink: 0, ahora si achicamos la pantalla ese item tratara de siempre ser de 300px, pero si agrandamos tomara mas de esos 300px.
**Siempre trata de no reducisse mas del ancho establecido para ese elemento, y si ya no cabe en la misma linea con los demas elemento bajara a una nueva linea, usandola completamente y SI SIGO ACHICANDO LA VENTANA SE DESBORDARA, ya que siempre tiene que ser de 300px MINIMOS.** 
**Con flex-shrink: 0; el ancho que le configuremos no se reducira, PERO SI SE PUEDE AGRANDAR, por lo que siempre va a tener 300px, pero si hay mas espacio disponible lo usara, YA QUE TENEMOS EL FLEX-GROW: 1; si sacamos el flex-grow no se agrandara.**
**Si sacamos el flex-wrap que esta configurado en el contenedor padre, este flex-wrap hace que los items no saltan a una nueva linea abajo, cuando hay poco espacio, entonces si lo sacamos y trenemos flex-shrink la caja se desbordara.** **Con el flex-wrap: wrap podemos hacer disenios RESPONSIVOS, ya que los elementos van pasando hacia abajo.**

## flex-basis
**flex-basis obliga a un item a tener una proporcion determinada**.
Agregamos la clase flex-basis-1, con una propiedad flex-basis y el valor 50%, **esto se lo agregamos a algun item, el 1, y este va a tener una proporcion del 50% con respecto al tamano disponible.** Si la pantalla es pequena quizas abarque una linea completa, pero si es mas grande puede que quede espacio para el resto de elementos. **Obligamos que un elemento tenga el 50% del tamano disponible.**
**Flex-basis tratara de abarcar la proporcion que le indicamos, pero si es muy pequena la ventana, se ira achicando junto al padre...**

## flex
Hacemos un segundo div contenedor dentro del contenedor padre, hacemos 3 nuevos elementos y le sacamos todos los estilos de item.
**Cremos una clase que contenga el flex grow, shrink y basis.** 
**En la clase flex-1, agregamos la propiedad flex: su valor corresponde a flex grow, lo dejamos en 1**, si esta clase se la agrego a todos los items, todos se distribuyen de la misma forma, **el primer valor de la PROPIEDAD FLEX es FLEX-GROW**.
Su siguiente valor es **flex-shrink**, **dentro de flex-1, flex: 1 0**, con esto lo diremos que NO SE ACHIQUEN LOS ELEMENTOS.
**El tercer valor es el flex-basis, flex: 1 0 300px, le doy 300px de flex-basis**, ahora si es que caben los 3 elementos con 300px los mostrara en una sola linea, pero si se achica alguno pasara a la parte inferior, **para que pase a la parte inferior NECESITO TENER EL FLEX-WRAP: WRAP en el CONTENEDOR PADRE, pero si la caja en inferior a los 300px, se desbordaran los items, ya que el flex-shrink esta en 0, ME IMPODI QUE LAS CAJAS SE ACHIQUEN MAS DE LOS 300PX... Si lo dejamos en 1, el flex-shrink, lo elementos si se achicaran aun mas!...**

## align-self
**Con esta propiedad le dicimos a un elemento hijo, que se posiciona donde queramos...**
Volvemos a crear un nuevo div dentro del div padre, con 3 items y sin clases de hijos...
A uno de estos items le damos alturo de 200px, y vemos que tenemos comportamiento stretch, todos los elementos demas elementos tratran de abarcar los 200px de altura.
**A la clase padre agramos un align-items: flex-end, los elementos sin la clase de altura, quedaran de su altura normal y quedan abajo..., PERO SI YO QUIERO QUE UNO DE ESTOS ITEMS NO QUEDE A LO MAS ABAJO, SINO QUE AL MEDIO O ARRIBA, PUEDO USAR EL ALIGN-SELF**
**Creo la clase align-self-start, su propiedad sera align-self: con el valor flex-start,** esto se lo agrego al elemento hijo que yo quiero que este en la parte superior...