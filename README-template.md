# Frontend Mentor - Order summary card solution

This is a solution to the [Order summary card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/order-summary-component-QlPmajDUj). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)
- [Acknowledgments](#acknowledgments)


## Overview

### The challenge

Users should be able to:

- See hover states for interactive elements

### Screenshot

#### Desktop Design

![](/screenshot/screenshot-desktop.png)

#### Mobile Design

![](/screenshot/screenshot-mobile.png)

### Links

- Solution URL: [solution repo on github](https://github.com/Akanni5/order-summary-component-main)
- Live Site URL: [vercel app site](https://your-live-site-url.com)

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

In the last challenge I solved. A nice fellow directed me to use the `<picture>` element whenever I have to use different images for different viewport sizes. For example, whenever I have two images for different viewports e.g, Mobile and Desktop. I normally used to create two `img`. I'll set its `display` to `none` depending on when viewport width.

Like this:

```html
<div class="hero-cover">
    <img src="/images/hero-cover-mobile.png" alt="hero cover" id="mobile-cover"/>
    <img src="/images/hero-cover-desktop.png" alt="hero cover" id="desktop-cover"/>
</div>
```
```css
#mobile-cover{
    display: none;
}

@media screen and (max-width: 475px){
    #mobile-cover{
        display: initial;
    }

    #desktop-cover{
        display: none;
    }
}
```

but, There's even a better way to write it. Using the ```<picture>``` tag, you'll get a better result with less code.


```html
<picture>
    <source media="(min-width: 650px)" srcset="images/pattern-background-desktop.svg">
    <img src="images/pattern-background-mobile.svg" alt="pattern background">
</picture>
```

`No CSS required.`


## Author

- Frontend Mentor - [@Akanni5](https://www.frontendmentor.io/profile/Akanni5)
- Twitter - [@coderoyalty](https://www.twitter.com/coderoyalty)

## Acknowledgments

Thanks to [@frank-itachi](https://www.frontendmentor.io/profile/frank-itachi) who informed me about the `<picture>` tag in html.