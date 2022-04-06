# CSS Demystified <!-- omit in toc -->

## Table of Contents <!-- omit in toc -->

- [Anatomy of a CSS Rule](#anatomy-of-a-css-rule)

## El Modelo de Caja

```css
.element {
  width: 200px;
  padding: 20px;
  border: 5px solid #9acc14;
  margin: 20px;
}
```

Inclusive si nosotros declaramos explícitamente una anchura: `width: 200px`. Realmente nuestro elemento
adquiere una anchura de **290px!**

`contenido(200px) + padding(40px [iz,de]) + borde(10px [iz,de]) + margen(40px [iz,de]) = 290px`

Para hacer nuestras vidas más fácil, es bastante común cambiar el `box-sizing` de un elemento a `border-box`.

```css
.element {
  box-sizing: border-box;
}
```

Ahora, cuando declaremos una anchura (o altura), también se incluirá el _padding_ y el _borde_. Además
del _contenido_, claro está.

`contenido,padding,borde(200px) + margen(40px [iz,de]) = 240px`

###### Tip 1

Hay que tratar de no asignarle un `heigh` a nuestros elementos, ya que esto puedo derivar desbordamientos y otros
errores. Y si por alguna razón es necesario poner un heigh, lo mejor es establecerlo como `min-heigh`. Una situación
bastante común es establecer un heigh porque necesitamos mayor espacio entre sección y sección, para este tipo de
casos lo mejor es simplemente agregar más `padding`.
