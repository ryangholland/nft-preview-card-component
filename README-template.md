# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./images/127.0.0.1_5500_index.html.png)

### Links

- Solution URL: [https://github.com/ryangholland/nft-preview-card-component]
- Live Site URL: [https://ryangholland.github.io/nft-preview-card-component]

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

This was a pretty easy one. The biggest challenge was getting the active state working for the NFT image. 

I used two backgrounds for the hover state: a low-opacity gradient and the image itself. 

I gave the eye SVG a normal state of hidden and used a pseudoclass combined with a child selector to make it visible when hovering over its parent container.

```css
.nft-image:hover {
  cursor: pointer;
  background: linear-gradient(
      0deg,
      hsla(var(--clr-cyan-hsl), 0.5),
      hsla(var(--clr-cyan-hsl), 0.5)
    ),
    url(./images/image-equilibrium.jpg);
  background-size: cover;
}

.hidden {
  visibility: hidden;
}

.nft-image:hover .hidden {
  visibility: visible;
}
```

### Useful resources

- [https://stackoverflow.com/questions/36679649/how-to-add-a-color-overlay-to-a-background-image] - Stack Overflow answer about adding a color overlay to a background image.
- [https://stackoverflow.com/questions/58190775/trying-to-make-a-div-appear-when-hovering-over-an-image] - Stack Overflow answer about using hover pseudoclass combined with a selector to change visibility property.

