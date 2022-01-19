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
## THE BOX MODEL

- The model includes the content area’s size (width and height) and the element’s padding, border, and margin. The properties include:

- width and height: The width and height of the content area.
padding: The amount of space between the content area and the border.
border: The thickness and style of the border surrounding the content area and padding.

- margin: The amount of space between the border and the outside edge of the element.

```CSS
/*Seperate*/
#img-one {
  margin-right: 20px;
  margin-left: 20px;
  margin-bottom: 30px;
  margin-top: 20px;
}

/*4 Values*/
/*clockwise rotation:
top,right,bottom,left */
p {
  margin: 6px 10px 5px 12px; 
}

/* 3 Values*/
/*If the left and right sides of the content can be equal: 
top,right&left,bottom*/
p {
  margin: 5px 12px 4px;
}

/*2Values*/
/*if the top and bottom sides can be equal, and the left and right sides can be equal
top&bottom, left&right*/
p {
  margin: 20px 10px;
}
```
- margin: 0 auto:The 0 sets the top and bottom margins to 0 pixels. The auto value instructs the browser to adjust the left and right margins until the element is centered within its containing element.
```CSS
/*Center the selector horizontally using the margin property*/
div.headline {
  width: 400px;
  margin: 0 auto;
}
```

- padding is space added inside an element’s border, while margin is space added outside an element’s border. One additional difference is that top and bottom margins, also called vertical margins, collapse, while top and bottom padding does not.

```CSS
/*
padding-top
padding-right
padding-bottom
padding-left
*/
p {
  padding-bottom: 10px;
}
```

- Border:
1. width—The thickness of the border. A border’s thickness can be set in pixels or with one of the following keywords: thin, medium, or thick.
2. style—The design of the border. Web browsers can render any of 10 different styles. Some of these styles include: none, dotted, and solid.
3. color—The color of the border. Web browsers can render colors using a few different formats, including 140 built-in color keywords.

- Border Radius: set all four corners of the border to a radius
```CSS
p {
  border: 3px solid coral;
  border-radius: 50%;
}
```

- The `overflow` property controls what happens to content that spills, or overflows, outside its box. The most commonly used values are:

- `hidden`—when set to this value, any content that overflows will be hidden from view.
- `scroll`—when set to this value, a scrollbar will be added to the element’s box so that the rest of the content can be viewed by scrolling.
- `visible`—when set to this value, the overflow content will be displayed outside of the containing element. Note, this is the default value.
```CSS
.donate{
  visibility: hidden;
}
```

## THE BOX MODEL REVIEW
- The box model comprises a set of properties used to create space around and between HTML elements.
- The height and width of a content area can be set in pixels or percentages.
- Borders surround the content area and padding of an element. The color, style, and thickness of a border can be set with CSS properties.
- Padding is the space between the content area and the border. It can be set in pixels or percent.
- Margin is the amount of spacing outside of an element’s border.
- Horizontal margins add, so the total space between the borders of adjacent elements is equal to the sum of the right margin of one element and the left margin of the adjacent element.
- Vertical margins collapse, so the space between vertically adjacent elements is equal to the larger margin.
- margin: 0 auto horizontally centers an element inside of its parent content area, if it has a width.
- The overflow property can be set to display, hide, or scroll, and dictates how HTML will render content that overflows its parent’s content area.
- The visibility property can hide or show elements.

## Resetting Defaults
```CSS
* {
  margin: 0;
  padding: 0;
}
```

## CHANGING THE BOX MODEL
- In the default box model, box dimensions are affected by border thickness and padding.
- The `box-sizing` property controls the box model used by the browser.
- The default value of the box-sizing property is `content-box`.
- The value for the new box model is `border-box`.
- The `border-box` model is not affected by border thickness or padding.
1. The default value of this property is `content-box`.
2. `box model`, the height and width of the box will remain fixed. 
```CSS
* {
  box-sizing: border-box;
}
```

