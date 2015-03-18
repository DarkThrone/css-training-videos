# Selectors specificity

## Info

__Demo__: http://codepen.io/DarkThrone/pen/bNQyaz
__Gist__: https://gist.github.com/DarkThrone/3807d1cdc41d816bee9e

## Description

Selector specificity determines which rules applies to an element given a set of selectors that collide. When two rule sets apply to the same element, the ones that are more specific alwasy trump over the less specific ones.

## Code

```html
<div class="container">
  <div>
    This is the first box
  </div>
  <div class="box">
    This is the second box
  </div>
</div>

<div class="container purple">
  <div>
    This is the first box
  </div>
  <div class="box">
    This is the second box
  </div>
</div>>
```

```css
.container {padding:40px;width:30%;}
.container div {width:150px;height:100px;margin:auto;}

div {
  background:lightgreen;
}

.container div {
  background: tomato;
}

.box {
  background: rebeccapurple;
  color: blue;
  border: 3px purple solid;
}

div.box {
  color: lightgreen;
}

.container.purple {
  background: lightblue;
}

.container.purple .box {
  background: rebeccapurple;
  color: peachpuff;
}
```

## Explanation

This examples shows the exact same html constructs but with different specificities. Pay special attention to the `div` with the `.box` class. The rules that collide in `.container div`, `div.box` and `.box` are a clear example of more specific selectors trumping over the less specific one.

You can check the [specificity algorithm here](http://www.w3.org/TR/selectors/#specificity).

You can see some articles with mre information in the following list:

- https://css-tricks.com/specifics-on-css-specificity/
- https://gist.github.com/getify/2956735
- http://stackoverflow.com/a/12743702

## Credits

email: Geronimo Garcia <geronimo.garcia@globant.com>
twitter: @geronimogarcia

