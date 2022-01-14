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