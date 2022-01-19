---
layout:     post
title:    CSS Review
subtitle:   BY Guanqiao Huang
date:       2019-01-14
author:     HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - CSS
---
## SETUP AND SYNTAX
- The basic anatomy of CSS syntax written for both inline styles and stylesheets.
- Some commonly used CSS terms, such as ruleset, selector, and declaration.
- CSS inline styles can be written inside the opening HTML tag using the style attribute.
- Inline styles can be used to style HTML, but it is not the best practice.
- An internal stylesheet is written using the `<style>` element inside the <head> element of an HTML file.
- Code inside `<style>` tags is written in CSS syntax and can include many selectors and rulesets.
- Internal stylesheets can be used to style HTML but are also not best practice.
- An external stylesheet separates CSS code from HTML, by using the “.css”.file extension.
- External stylesheets are the best approach when it comes to using HTML and CSS.
- External stylesheets are linked to HTML using the `<link>` element.

## SELECTORS
- CSS can select HTML elements by type, class, ID, and attribute.
- All elements can be selected using the universal selector.
- An element can have different states using the pseudo-class selector.
- Multiple CSS classes can be applied to one HTML element.
- Classes can be reusable, while IDs can only be used once.
- IDs are more specific than classes, and classes are more specific than type. That means IDs will override any styles from a class, and classes will override any styles from a type selector.
- Multiple selectors can be chained together to select an element. This raises the specificity but can be necessary.
- Nested elements can be selected by separating selectors with a space.
- Multiple unrelated selectors can receive the same styles by separating the selector names with commas.
-  IDs are the most specific, because they should only be used on a single element.

## VISUAL RULES
- The `font-family` property defines the typeface of an element.
- `font-family` allows you to apply a typeface to a particular selector
- `font-size` controls the size of text displayed.
- `font-weight` defines how thin or thick text is displayed.
- `font-weight` sets the thickness of letters in text.
- The `text-align` property places text in the left, right, or center of its parent container.
- Text can have two different color attributes: `color` and `background-color`. color defines the color of the text, while `background-color` defines the color behind the text.
- CSS can make an element transparent with the `opacity` property.
- `opacity` values range from 0 (transparent) to 1 (opaque).
- CSS can also set the background of an element to an image with the `background-image` property.
- The `!important` flag will override any style, however it should almost never be used, as it is extremely difficult to override.
- The `!important` rule will override the other color declarations.

```CSS
.header{
  background-color:CornflowerBlue ;
  text-align: center;
}

.about-me{
  font-size:20px;
  opacity:0.5;
}

.title{
  font-weight:bold;
}

h1{
  color: Azure;
}

body{
  font-family:Georgia;
  background-image: url('https://content.codecademy.com/courses/learn-css-selectors-visual-rules/hypnotize_bg.png')
}


```

The model includes the content area’s size (width and height) and the element’s padding, border, and margin. The properties include:

width and height: The width and height of the content area.
padding: The amount of space between the content area and the border.
border: The thickness and style of the border surrounding the content area and padding.
margin: The amount of space between the border and the outside edge of the element.

- padding is space added inside an element’s border, while margin is space added outside an element’s border. One additional difference is that top and bottom margins, also called vertical margins, collapse, while top and bottom padding does not.