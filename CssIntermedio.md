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



## Buenas practicas
Siempre crear clases especificas para algo, para luego poder ir reutilizando, como las funciones...
Siempre separar los estilos en diferentes clase, asi se le pueden aplicar a diferentes etiquetas. Siempre ir desde lo mas general a lo especifico. Lo doy estilos generales a los parrafos, pero a cada parrafo especifico le agrego sus estilos propios, ejemplo formateo los parrafos de una forma general, y cambio el color de cada uno. Estructurar los estilos, los colores juntos, los espaciados juntos...