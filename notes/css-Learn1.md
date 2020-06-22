# CSS Learn Part 1A

Reference: [Udemy Course](https://www.udemy.com/course/advanced-css-and-sass/)

## CSS Cool Tricks Cheatsheet 😎

For reference check [Gihub repositoryhttps://github.com/fbohz/css-learning/tree/master/museo-demo](https://github.com/fbohz/css-learning/tree/master/museo-demo).

**`box-sizing: border-box`**

 With box-sizing: border-box;, we can change the box model to what was once the “quirky” way, where an element’s specified width and height aren’t affected by padding or borders. This has proven so useful in responsive design that it’s found its way into reset styles. So border-box can help make responsive layouts more manageable.


**`clip-path: polygon()`**

You specify polygon you want to add the clipping you add clippings with x and y coordinates left to right.  Use [Clippy tool](https://bennettfeely.com/clippy/) to calculate it for you!

**CSS Animations with `@keyframes` and `animation`**

We use `@keyframes` and then give animation a name. Then you specify what happens when animation starts, ends and anything in the middle.

```css
@keyframes moveInLeft {
0% {
 opacity: 0;
 transform: translateX(-100px);
}

100% {
 opacity: 1;
 transform: translate(0);
}
}
```

Then once you define it, you can add it to the specific element you want to apply with `animation` keyword.

```css
.btn-animated {
/* animation name, animation duration
    animation timing function, 
    animation delay
*/
animation: moveInBottom .5s ease-out .75, 
}
```

**Pseudo Elements and Pseudo Classes**

Pseudo classes are special state of a selector. For example `.btn:link` selects the elements on a special condition in this case when as link.

Pseudo elements allow us to select certain part of an element. They are denoted with two colons to differentiate them from pseudo classes. This is the syntax:

```css
selector::pseudo-element {
  property: value;
}
```

There are various pseudo elements. Take a sneak peak and learn more about them [here](https://blog.logrocket.com/a-guide-to-css-pseudo-elements/).

**`box-shadow`**

With box shadow you can add shadow to elements. Take a look at the [box shadow generator](https://www.cssmatic.com/box-shadow).

## Resources
<p>👉&nbsp;<a rel="noopener noreferrer" href="https://github.com/jonasschmedtmann/advanced-css-course">Udemy Course material and instructions on GitHub</a></p>
<p><a rel="noopener noreferrer" href="http://codingheroes.io/resources/">👉 Udemy resources page</a></p>
[Emmet Cheat Sheet](https://docs.emmet.io/cheat-sheet/)
[Box Sizing](https://css-tricks.com/box-sizing/)
