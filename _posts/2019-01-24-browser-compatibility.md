---
layout:     post
title:     Browser compatibility
subtitle:   BY Guanqiao Huang
date:       2019-01-23
author:     HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - CSS
---

1. Browsers have different default styles for HTML elements which will result in discrepancies in how they are rendered across browsers.
2. Avoid using the latest CSS features that have yet to be supported by most modern browsers.
3. Polyfills can be used to provide modern functionality in older browsers that do not natively support it.
4. Browsers have different default styles for HTML elements.

Common vendor prefixes include:

- -webkit- for Chrome, Safari, newer versions of Opera, and almost all iOS browsers, including Firefox for iOS
- -moz- for Firefox
- -ms- for Internet Explorer and Microsoft Edge
- -o- for old pre-WebKit versions of Opera

## Example
```CSS
.tilted {
  -webkit-transform: rotate(15deg);
  -moz-transform: rotate(15deg);
  -ms-transform: rotate(15deg);
  -o-transform: rotate(15deg);
  transform: rotate(15deg);
}

strong{
	color: chocolate;
  font-weight: bold;
  background: url('flowers.jpg');
  background-size: cover;
	background-clip: text;
  /* Set background-clip to text with approporate prefix for Chrome */
  -webkit-background-clip: text;
	color: transparent;
}
```

## Resources

- Use polyfill tools like [Modernizr](https://github.com/Modernizr/Modernizr) or [Polyfill.io](https://github.com/financial-times/polyfill-service) to automatically check and apply polyfills.
- Use tools like [Autoprefixer](https://github.com/postcss/autoprefixer) to automactically include all vendor prefixes for the features that require them.
- [Browser Defaults Styles](https://browserdefaultstyles.com/)
- [Browser support table](https://caniuse.com/)