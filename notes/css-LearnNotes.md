# CSS Learn Part 1

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

With the `inherit` keyword we force inheritance.

**Visual Formatting Model**

The Visual Formatting Model is an algorithm that calculates boxes and determines the layout of these boxes, for each element in the render tree, in order to determine the final layout of the page.

*Box model*

![Screen Shot 2020-06-23 at 1 00 31 PM](https://user-images.githubusercontent.com/15071636/85438386-8bc2cf80-b551-11ea-86fb-71995f347ae6.png)

*Heights and Widths*

![Screen Shot 2020-06-23 at 1 01 07 PM](https://user-images.githubusercontent.com/15071636/85438499-b1e86f80-b551-11ea-9879-e0d89a95d2e5.png)

*Box Size Property as Border-box*

This will set as width and height specified by just width and height.

![Screen Shot 2020-06-23 at 1 02 30 PM](https://user-images.githubusercontent.com/15071636/85438771-eceaa300-b551-11ea-8a51-b767df986fc8.png)

*Box Types*

![Screen Shot 2020-06-23 at 1 04 50 PM](https://user-images.githubusercontent.com/15071636/85439024-2ae7c700-b552-11ea-8e30-b567b7f9cafa.png)

*Position Schemes*

![Screen Shot 2020-06-23 at 1 06 32 PM](https://user-images.githubusercontent.com/15071636/85439241-62567380-b552-11ea-918e-b1bdd0f71cf8.png)

*Stacking Contexts*

Are like layers that form a stack. You can use `z-index` to create static context with `transform()` as well.

**CSS Architecture, Components and BEM**

Use this architect mindset:

![Screen Shot 2020-06-23 at 1 11 06 PM](https://user-images.githubusercontent.com/15071636/85439812-050ef200-b553-11ea-9516-50d507358b19.png)

*Use component driven design*

![Screen Shot 2020-06-23 at 1 12 09 PM](https://user-images.githubusercontent.com/15071636/85439950-2c65bf00-b553-11ea-99ee-6922e05a841e.png)

*Block Element Modifier (BEM)*

Used to name elements.

*Logic Folder Structure*

![Screen Shot 2020-06-23 at 1 15 07 PM](https://user-images.githubusercontent.com/15071636/85440365-93837380-b553-11ea-9604-8fa976b5ce63.png)

You don't need to use all folders, just what you need.

## CSS Cool Tricks Cheatsheet 😎

For reference check [Github repositoryhttps://github.com/fbohz/css-learning/tree/master/museo-demo](https://github.com/fbohz/css-learning/tree/master/museo-demo).

**Three Pillars to write good CSS**

1. *Responsive Design*: Build website that works well on all devices. You'll have to know about fluid layouts, media queries, responsive images, correct units (for e.g. font sizes) and desktop-first vs mobile-first.
2. *Writing maintainable/scalable code*: Write code that is clean and reusable. Think about CSS folder architecture, and class naming.
3. *Web Performance*: Make it faster and smaller in size. Less HTTP request, compress code, use CSS preprocessor. Also less images and compress images.

**Converting `px` units to `rem`**

Remember rem is related to root font size so by setting the root font size then use rem you can easily make changes to root without changing all lines of codes. You can specify root font size as this. Now but having root font size as px we could better use percentages. 

```css
html {
    font-size: 62.5%;
}
```

Since usually font size is 16px here we are saying 62.5% which is roughly 10px. This will mean that 1rem is 10px, 2rem is 20px and so forth. You can use rem as this:

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

### Resources
<p>👉&nbsp;<a rel="noopener noreferrer" href="https://github.com/jonasschmedtmann/advanced-css-course">Udemy Course material and instructions on GitHub</a></p>
<p><a rel="noopener noreferrer" href="http://codingheroes.io/resources/">👉 Udemy resources page</a></p>
[Emmet Cheat Sheet](https://docs.emmet.io/cheat-sheet/)
[Box Sizing](https://css-tricks.com/box-sizing/)

## Introduction to SASS

SASS is CSS preprocessor an extension to CSS to add more power. So you write code in SASS files then the SASS compiler compiles it into CSS.

SASS gives us:

![Screen Shot 2020-06-24 at 9 45 53 AM](https://user-images.githubusercontent.com/15071636/85578207-87ed8680-b5ff-11ea-89de-fce958c15780.png)

There are *two SASS syntax*

![Screen Shot 2020-06-24 at 9 47 24 AM](https://user-images.githubusercontent.com/15071636/85578561-c5eaaa80-b5ff-11ea-9cb8-d056cb6a7f6d.png)

SCSS is easier to learn and preferred than Sass.

If you want to play with SASS without installing it first just use [Codepen](https://codepen.io/).

**Implement Nesting With SASS**

In SASS you can do 

```css
.navigation {
  list-style: none;

  li {
    display: inline-block;

    &:first-child {
      margin: 0;
    }
  }
}
```

Note `&` replaces selectors up to the point so will be `.navigation li:first-child`. SCSS above is the equivalent in vanilla CSS as:

```css
.navigation {
 list-style: none;
}

.navigation li {
 display: inline-block;
}

.navigation li:first-child {
  margin: 0;
}
```

**Mixins, Extends and Functions**

*Mixin* is a reusable piece of code. Let's say we want to implement a [Clearfix](https://www.w3schools.com/howto/howto_css_clearfix.asp) in multiple places. We use the `@mixin` keyword to define it and `@include` where we want to use it.

```css
@mixin clearfix {
 &:after {
     content: "";
     clear: both;
     display: table'
 }   
}

nav {
 @include clearfix;
}
```

You can also pass in variables to mixin definitions, just make sure when you want to use it also pass in the variable for the mixin to work. Mixins then do become like functions. We could also define functions with the `@function`. Mixins however are used more.

*Extends* is like writing a placeholder then extend those placeholder. We write placeholders with `%` sign. Then we use it with the `@extend` keyword. Only use extends if rules are related. Again, mixins are used more. Do look up and note the difference between extends and mixins.

**Compiling Sass and Hot Reloading**

Remember to install first. Then you can compile by adding this script in package.json:

```json
"scripts": {
 "compile:sass": "node-sass sass/main.scss css/style.css -w
},
```

The `-w` will keep watching for whatever we do in our code. You can also install `npm i live-server -g`. Then run it as `live-server` on root folder. For the changes to be reflected without needing to reload manually.


## Responsive Design Layouts and Design Principles

Consider these basic principles:

![Screen Shot 2020-06-24 at 5 29 36 PM](https://user-images.githubusercontent.com/15071636/85634127-577a0c80-b640-11ea-8e7d-0a10e965094c.png)

There are 3 major types.

- Float Layouts
- Flexbox
- CSS Grid

Note Float is the oldest method.

**Custom Grid With Floats**

We build them with columns and rows in mind. 


# CSS Learn Part 2A

## Responsive Design

**Desktop vs Mobile First**

![Screen Shot 2020-06-28 at 10 19 08 AM](https://user-images.githubusercontent.com/15071636/85951445-ddd86c00-b928-11ea-996e-cd2aa10dfc33.png)

Mobile first is very bare minimal but might end up very limited on desktop.

Pros vs. Cons

![Screen Shot 2020-06-28 at 10 26 27 AM](https://user-images.githubusercontent.com/15071636/85951618-e1202780-b929-11ea-83d7-0d43d26a06ea.png)

Both are important.

**Max Width vs Min-Width Media Queries**

![Screen Shot 2020-06-28 at 10 22 56 AM](https://user-images.githubusercontent.com/15071636/85951552-5ccda480-b929-11ea-9beb-1e3ddb2da9ba.png)

Now if there are conflicting rules in media queries then the **last query will apply**.

**Breakpoints**

Is where we want our design to change. Here's a good method that uses [screen resolution stats](https://gs.statcounter.com/screen-resolution-stats).

![Screen Shot 2020-06-28 at 10 38 23 AM](https://user-images.githubusercontent.com/15071636/85951866-88518e80-b92b-11ea-942e-36ad550cf9cc.png)


## Responsive Images

Responsive images means sending the right image to the right device. So smaller images to smaller screens. Some techniques:

![Screen Shot 2020-06-28 at 6 37 49 PM](https://user-images.githubusercontent.com/15071636/85961209-878e1c00-b96e-11ea-8c02-aeeb87a3e025.png)

## Browser Support

[Can I Use](https://caniuse.com/), for browser support checking.

You can do graceful degradation with `@supports`. Example:

```css
@supports (-webkit-backdrop-filter: blur(10px)) or (backdrop-filter: blur(10px)) {
    -webkit-backdrop-filter: blur(10px);
    backdrop-filter: blur(10px);
    background-color: rgba($color-black, .3);
}
```

## Build Processes

We can implement simple NPM build processes after we finish a feature.

![Screen Shot 2020-06-28 at 7 35 10 PM](https://user-images.githubusercontent.com/15071636/85962487-9a0c5380-b976-11ea-8dae-b021b308f223.png)

We do this on `package.json`, check it on [Github repository](https://github.com/fbohz/css-learning/blob/master/museo-demo/package.json).

There are a couple of NPM packages we use, we can install as `npm i concat --save-dev`, `npm i autoprefixer --save-dev`, `npm i postcss-cli --save-dev`, `npm i npm-run-all --save-dev`.

Also note the `--parallel` flag on start. It means both run at the same time.

So to run all you'll just do:

`npm run build:css`

And your css will be compiled, concat, compressed and ready for production! 