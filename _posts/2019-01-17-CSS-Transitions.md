---
layout:     post
title:    CSS Transitions
subtitle:   BY Guanqiao Huang
date:       2019-01-17
author:     HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - CSS
---

## TRANSITIONS

[Links](https://www.youtube.com/watch?v=_DQfgsuURCU&feature=youtu.be)
Different properties transition in different ways, for example:

- Color values, like color and background-color, will blend to a new color.
- Length values like font-size, width, and height will grow or shrink.
- Duration is specified in seconds or milliseconds, such as 3s, 0.75s, 500ms. The default value is 0s, or instantaneous, as if there is no transition.
```CSS
a {
  display: block;
  width: 300px;
  padding: 31px 5px;
  border-radius: 5px;
  margin: 20% auto;
  background-color: orange;
  text-align: center;
  font-family: Helvetica;
  font-size: 32px;
  color: mintcream;
  transition-property: background-color;
  transition-duration: 750ms;
}

a:hover {
  background-color: limegreen;
}

```

## Timing Function
- ease-in — starts slow, accelerates quickly, stops abruptly
- ease-out — begins abruptly, slows down, and ends slowly
- ease-in-out — starts slow, gets fast in the middle, and ends slowly
- linear — constant speed throughout

## Delay
Our last transition property is transition-delay. Much like duration, its value is an amount of time. Delay specifies the time to wait before starting the transition. As with the duration property, the default value for transition-delay is 0s, which means no delay.

## Shorthand
The properties must be specified in this order: transition-property, transition-duration, transition-timing-function, transition-delay.
```CSS
transition: color 1.5s linear 0.5s;
```

```CSS
html,
body {
  margin-top: 50px;
  height: 100%;
  text-align: center;
  font-family: Arial, sans-serif;
  font-size: 16px;
}

h1 {
  font-size: 40px;
}

.game {
  position: relative;
  display: inline-block;
  height: 60%;
}

.game img {
  cursor: pointer;
}

.game .safari {
  margin-top: 50px;
  height: 430.188px;
  width: 573.578px;
}

.game .gazelle {
  position: absolute;
  top: 260px;
  left: 231px;
  z-index: 1;
  max-height: 50px;
  /*
  transition-property: max-height;
  transition-duration: 750ms;
  transition-timing-function: linear;
  transition-delay: 400ms;
  */
  transition: max-height 750ms linear 400ms;
}

.game .gazelle:hover {
  max-height: 180px;
}
```

```CSS
@import url(https://fonts.googleapis.com/css?family=Open+Sans);
@import url(https://maxcdn.bootstrapcdn.com/font-awesome/4.3.0/css/font-awesome.min.css);

/* Main Styles */
body {
  min-width: 300px;
  background-color: #ecf0f1;
  font-family: 'Open Sans', sans-serif;
  font-size: 16px;
}

.button {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  display: block;
  overflow: hidden;
  margin: auto;
  border-radius: 5px;
  box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.3);
  width: 300px;
  height: 100px;
  line-height: 100px;
  background-color: #34B3A0;
  color: #fff;
}

.button span,
.button .icon {
  position: absolute;
  display: block;
  height: 100%;
  text-align: center;
}

.button span {
  width: 72%;
  left: 0px;
  line-height: inherit;
  font-size: 22px;
}

.button .icon {
  right: 0;
  width: 28%;
}

.button .icon .fa {
  font-size: 30px;
  vertical-align: middle;
}

.icon {
  width: 200px;
  background-color: #1A7B72;
}

.button:hover span {
  left: -72%;

}

.button:hover .icon {
  width: 100%;
}

.button:hover .icon .fa {
  font-size: 45px;
}

.button span,
.button div,
.button i {
  /*
  transition: width 750ms ease-in 200ms, 
              left 500ms ease-out 450ms,
              font-size 950ms linear;
 */
 transition: all 1.2s ease-out 0.2s;

}

```

```CSS
/* Universal Styles */

html {
  font-size: 16px;
}

body {
  min-width: 475px;
  font-family: "Cormorant Garamond", serif;
}

@media only screen and (max-width: 810px) {
  html {
    font-size: 14px;
  }
}


@media only screen and (max-width: 540px) {
  html {
    font-size: 12px;
  }
}

/* Navigation Bar */

nav {
  position: fixed;
  z-index: 5;
  left: -17.8em;
  display: flex;
  align-items: center;
  height: 100%;
  padding-left: 5rem;
  padding-right: 2rem;
  background: url("https://content.codecademy.com/courses/freelance-1/unit-6/nav_background.png") center center repeat;
  font-family: "Proza Libre", serif;
  font-size: 18px;
  line-height: 2.2;
  font-weight: bold;
  color: #142033;

  transition-property: left;
  transition-duration:1s;
  transition-timing-function: ease-out;
  transition-delay:200ms;

}

nav:hover {
  left: 0;
}

nav .hover-content {
  margin-right: 3em;
}

nav h2 {
  font-family: "Cormorant Garamond", serif;
  font-size: 2.6em;
  font-weight: bold;
  color: #639eff;
}

nav h3 {
  padding-bottom: 1.1em;
}

nav ol {
  list-style: upper-roman outside;
}

nav a {
  text-decoration: none;
  color: inherit;
  transition: color 800ms ease-in 300ms;
}

nav a:hover,
nav a.active {
  color: #639eff;
}

/* Header */

header {
  padding: 3.125rem 13rem;
  background-color: #142033;
  text-align: center;
  font-weight: bold;
  line-height: 2.1;
  color: #b3d0ff;
}

header h1 {
  font-size: 6rem;
  line-height: 1;
  font-weight: 500;
  color: #66a1ff;
}

header em {
  font-size: 1.5rem;
  font-style: italic;
}

header h2 {
  font-size: 3rem;
}

@media only screen and (max-width: 810px) {
  header {
    padding: 3.125rem 8rem 3.125rem 10rem;
  }

  header h1 {
    font-size: 4rem;
  }

  header h2 {
    font-size: 2rem;
  }
}

/* Book Content */

.book-content {
  padding: 4.75rem 20%;
  background-color: #f2f7ff;
  font-family: "Proza Libre", sans-serif;
  font-size: 1.5rem;
  line-height: 2;
  color: #4a4a4a;
  cursor: default;
}

.book-content h3 {
  text-align: center;
  font-size: 3rem;
  line-height: 2.1;
  font-weight: bold;
  color: #142033;
}

.chapter {
  color: #639eff;
}

.chapter .number {
  display: block;
  font-size: 1.25rem;
}

.chapter .name {
  display: block;
  font-size: 2.25rem;
}

.book-content .prose {
  margin-bottom: 4.75rem;
}

@media only screen and (max-width: 810px) {
  .book-content {
    padding-right: 10%;
  }
}

@media only screen and (max-width: 540px) {
  .book-content {
    padding-right: 1%;
  }
}

/* Word Definitions */

.definable {
  display: inline;
}

.definable .word {
  color: #639eff;
  transition: color 300ms ease-in;
}

.definable .word:hover {
  color: #306acc;
}

.definable .definition-container {
  position: fixed;
  z-index: 10;
  top: -100%;
  left: 0;
  box-sizing: border-box;
  width: 100%;
  padding: 0.5rem 4rem 2rem 4rem;
  background-color: #ffffff;
  box-shadow: 0 0 64px 0 rgba(0, 0, 0, 0.2);
  opacity: 0;
  font-family: "Proza Libre", sans-serif;
  font-size: 1.5rem;

  transition-property: top, opacity;
  transition-duration: 2000ms, 3000ms;
  transition-delay: 0s, 1000ms;
}

.definable:hover .definition-container {
  top: 0;
  opacity: 1;
}

.definition-container h4 {
  font-family: "Cormorant Garamond", serif;
  font-size: 3rem;
  font-weight: bold;
  line-height: 2.1;
  color: #66a1ff;
}

.definition-container .information {
  display: block;
  line-height: 2.5;
  color: #9b9b9b;
}

.definition-container .definitions {
  list-style: inside decimal;
  line-height: 1.7;
  color: #4a4a4a;
}

/* Chapter Navigation Buttons */

.navigation-buttons {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.button {
  display: inline-flex;
  justify-content: space-between;
  align-items: center;
  width: 13rem;
  padding: 0 2rem;
  background-color: #639eff;
  opacity: 0.3;
  font-size: 3rem;
  font-weight: bold;
  text-decoration: none;
  color: #ffffff;

  transition-property:opacity;
  transition-duration: 500ms;
  transition-timing-function: ease-in-out;
  transition-delay:300ms;
}

.button:hover {
  opacity: 1;
}

@media only screen and (max-width: 930px) {
  .button {
    width: auto;
    padding: 1rem 2rem;
  }

  .button .action {
    display: none;
  }
}
```