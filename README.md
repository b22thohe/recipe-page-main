# Frontend Mentor - Recipe page solution

This is a solution to the [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

### The challenge

- Build out this recipe page and get it looking as close to the design as possible.

### Screenshot

![screenshot](./screenshot.jpg)

### Links

- Solution URL: [Github Repository](https://github.com/b22thohe/recipe-page-main)
- Live Site URL: [Github live site](https://b22thohe.github.io/recipe-page-main/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Mobile-first workflow

### What I learned

I ran into some trouble on how to style the preparation info list. According to the design it's supposed to be an unordered list with bullets. Since the bullets themselves
are not elements, I cannot apply padding to them. One solution would of course be to manipulate the ul and/or the li items, but that could cause a headache down the road. 
Well, after a bit of research I found the CSS property list-style-position. Setting it to "inside" [the content box] immediately solved the whole problem with padding on the list items.

```css
ul.preparation-list {
  list-style-position: outside;
}
```

Another problem that arose after a while was that I wanted to use the header tag for semantic purposes. But when looking it up there was no clear indication what should actually goe into
the header element. Most sources I checked often suggest a cover image and an h1 element. But for this particular page, I think the preamble should logically be grouped with the h1 element,
so I decided at first to just put the image in the header. But that posed a problem when doing the styling for desktop screens when I wanted to give the body another background color than
the rest of the content. I could have placed a div around the heading and the rest of the content (main element), but that didn't seem like a good semantic choice. So I ultimately decided
on removing the header element completely and just put the image inside the main element along with the rest of the elements. That way I could give the body element one background color,
and the rest another color. The takeaway from this is that there will always come situations where you have to compromise and choose between semantics and practicality, and it is good to
decide beforehand what you should prioritize when that happens.   

### Continued development

On desktop (1440px) the main tag is made narrower than the body, showing the latters different background color. It makes for a easier read when your eyes don't have to read the full page
width. If and when I go back to iterate the design for this I'd like to start that narrower main tag design earlier to make the responsive layout more fluent as the user changes screen size.
But for now I just stick with the two defined sizes (375px and 1440px).

## Author

- Website - [Thomas Helsing](https://codingsteps.online/)
- Frontend Mentor - [@b22thohe](https://www.frontendmentor.io/profile/b22thohe)
