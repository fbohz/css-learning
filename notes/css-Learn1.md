# CSS Learn Part 1A

Reference: [Udemy Course](https://www.udemy.com/course/advanced-css-and-sass/)

## CSS Under-the-hood

**What happens to CSS when we load a website**

![Screen Shot 2020-06-23 at 11 47 02 AM](https://user-images.githubusercontent.com/15071636/85431567-56b17f80-b547-11ea-9999-c115a35350ec.png)

**The Cascade and Specificity**

The cascade is the process of combining different stylesheets and resolving conflicts between different CSS rules and declarations, when more than one rule applies to a certain element. There could be app, user, browse declaration.

The cascade works by:

- Importance
- Specificity 
- Source order

![Screen Shot 2020-06-23 at 11 54 05 AM](https://user-images.githubusercontent.com/15071636/85432236-49e15b80-b548-11ea-8028-2e1c5ada89e1.png)

Have in mind:

![Screen Shot 2020-06-23 at 11 58 12 AM](https://user-images.githubusercontent.com/15071636/85432652-e277db80-b548-11ea-8f86-3365f1967801.png)

**How CSS Values are Processed**

![Screen Shot 2020-06-23 at 12 15 26 PM](https://user-images.githubusercontent.com/15071636/85434171-41d6eb00-b54b-11ea-9cdd-5a1ad93f8245.png)

*How are units converted from relative to absolute (px)?*

![Screen Shot 2020-06-23 at 12 26 45 PM](https://user-images.githubusercontent.com/15071636/85435278-d4c45500-b54c-11ea-84d1-8af6929baabe.png)

*Value Processing reminders*

![Screen Shot 2020-06-23 at 12 27 31 PM](https://user-images.githubusercontent.com/15071636/85435350-ef96c980-b54c-11ea-8f12-43bf957fb2db.png)

**Inheritance**

![Screen Shot 2020-06-23 at 12 30 51 PM](https://user-images.githubusercontent.com/15071636/85435644-66cc5d80-b54d-11ea-8ba8-48ba22ef564f.png)

*Most important things to know about inheritance*

![Screen Shot 2020-06-23 at 12 32 07 PM](https://user-images.githubusercontent.com/15071636/85435787-9aa78300-b54d-11ea-9958-bc4455b88e6f.png)



## CSS Cool Tricks Cheatsheet 😎

For reference check [Gihub repositoryhttps://github.com/fbohz/css-learning/tree/master/museo-demo](https://github.com/fbohz/css-learning/tree/master/museo-demo).

**Three Pillars to write good CSS**

1. *Responsive Design*: Build website that works well on all devices. You'll have to know about fluid layouts, media queries, responsive images, correct units (for e.g. font sizes) and desktop-first vs mobile-first.
2. *Writing maintainable/scalable code*: Write code that is clean and reusable. Think about CSS folder architecture, and class naming.
3. *Web Performance*: Make it faster and smaller in size. Less HTTP request, compress code, use CSS preprocessor. Also less images and compress images.

**Converting `px` units to `rem`**

Remember rem is related to root font size so by setting the root font size then use rem you can easily make changes to root without changing all lines of codes. You can specify root font size as this:

```css
html {
    font-size: 10px;
}
```

This will mean that 1rem is 10px, 2rem is 20px and so forth. You can use rem as this:

```css
.logo-box {
 position: absolute;
 /* 4rem = 40px */
 top: 4rem; 
 left: 4rem;
}
```

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
