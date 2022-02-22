# CSS Demystified <!-- omit in toc -->

## Table of Contents <!-- omit in toc -->

- [Anatomy of a CSS Rule](#anatomy-of-a-css-rule)

## The Box Model

```css
.element {
  width: 200px;
  padding: 20px;
  border: 5px solid #9acc14;
  margin: 20px;
}
```

So even though we've declared `width: 200px` we have an element with an actual width of 290px!

To help make our lives easier, it's very common to change the `box-sizing` of and element to `border-box`.

```css
.element {
  box-sizing: border-box;
}
```

Now, when we declare a width (or heigh), the number we declare includes the **content**, but also includes
the **padding** and **border**.
