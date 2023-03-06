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
