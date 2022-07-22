# Frontend Mentor - Scoot website solution

This is a solution to the [Scoot website challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/scoot-multipage-website-N76alNPRJ). 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Improvements](#improvements)
 


## Overview

### The challenge

Users should be able to:

- View the optimal layout for each page depending on their device's screen size
- See hover states for all interactive elements throughout the site

### Screenshot

![](./screenshot.jpg)

### Links

- Live Site URL: [Live link](https://eclecticowl.github.io/scoot-multi-page-website/)

## My process

### Built with

- SASS
- Vue.js

### What I learned

I learned about Vue's built in transition component. While I could have just set it up an accordion to use without it, it's fun to try new concepts.
Perhaps I will use it in future projects as well.

```html
<div class="faq-item">
	<div class="faq-title" @click="show3 = !show3">
		<span>Should I wear a helmet?</span>
		<img v-if="show3" src="@/assets/icons/chevron.svg?inline" alt="chevron denoting whether the item is closed">
		<img class="invert" v-else src="@/assets/icons/chevron.svg?inline" alt="chevron denoting whether the item is closed">
	</div>
		<Transition name="fade">
			<p v-if="show3">Yes, please do! All cities have different laws. But we strongly strongly strongly recommend 
  always wearing a helmet regardless of the local laws. We like you and we want you to be as 
  safe as possible while Scooting.</p>
		</Transition>
</div>
```
```css
.fade-enter-active, .fade-leave-active 
  transition: opacity .5s ease
.fade-enter-from, .fade-leave-to 
  opacity: 0
```

### Improvements

- Adding a bunch of show variables is a bit too messy. I need to think of some alternatives to reduce this down.



