---
layout: post
title: JavaScript Request
subtitle: BY Guanqiao Huang
date: 201-01-02
author: HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
  - JavaScript
---

## XHR GET Requests II
```JS
/* written the boilerplate code for an AJAX GET request using an XMLHttpRequest object.*/
const xhr = new XMLHttpRequest(); 
const url =  'https://api-to-call.com/endpoint';
xhr.responseType = 'json';
xhr.onreadystatechange = () => {
  if (xhr.readyState === XMLHttpRequest.DONE) {
    return xhr.response;
}};

xhr.open('GET', url);
xhr.send();
```

## XHR GET Requests II

```JS
/*you will incorporate that boilerplate code to make a GET request to the Datamuse API to search for words that rhyme!*/

```

## Links
[JS Diagram XHR](https://content.codecademy.com/courses/intermediate-javascript-requests/diagrams/XHR%20GET%20diagram.svg)
[XML introduction](https://developer.mozilla.org/en-US/docs/Web/XML/XML_introduction)
[Datamuse](https://www.datamuse.com/api/)
[XHR GET Requests III](https://www.codecademy.com/workspaces/61f8e7c48f6c970a7a049534)