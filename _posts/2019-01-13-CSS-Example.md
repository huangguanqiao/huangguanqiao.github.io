---
layout:     post
title:    CSS Example
subtitle:   BY Guanqiao Huang
date:       2019-01-13
author:     HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - CSS
---

## Stylesheet
### Internal Stylesheet
```CSS
<style>
selector {
  //declaration
  property: value;
}
</style>
```

### External Stylesheet
`<link href='./style.css' rel='stylesheet'>`

### Universal
```CSS
* {
  property: value;
}
```

- CSS is not limited to selecting elements by their type.
- HTML elements can also have [attributes](https://www.w3schools.com/html/html_attributes.asp)
- 如果是全局用`*`号
- 如果是标准type selector 不用符号直接名字，比如`h1{}`
- 如果是class selector 用`.`符号来开头，比如`.brand{}`
- 假如是ID selector 用`#`符号来开头，比如`#brand{}`用在`<h1 id='brand'> ... </h1>`
- The uppercase class name should be next to the title class name, with a space in between. 比如`<h1 class='title uppercase'>ABC</h1>`
```CSS
.title {
  color: teal;
}

.uppercase{
  text-transform: uppercase;
}
```

- 如果是Attribute selector， 可以用`[]`，比如[href]{}
```CSS
//html
<img src='/images/seasons/cold/winter.jpg'>
<img src='/images/seasons/warm/summer.jpg'>

//CSS
img[src*='winter'] {
  height: 50px;
}
 
img[src*='summer'] {
  height: 100px;
}
```
意思是链接包括某string，用某stytle。比如对于`<img>`来说`src*='string'`，比如对于`<a>`来说`href*='string'`。
The first ruleset looks for an img element with an attribute of src that contains the string 'winter', and sets the height to 50px.

### Pseudo-class
鼠标移动到selector的变化
```CSS
selector:pseudo-class {
 
}
```

### Chaining
```CSS
elements.classname{}

//example
//意思是标有destination作为class的<h2>
//比如<h2 class='destination heading-background'>
h2.destination{
  font-family: Tahoma;
}
```

### Descendant Combinator
```CSS
.Classname nestedelements{

}

//example
//意思是description这个class里面的<h5>
.description h5{

}
```

### Chaining and Specificity
```CSS
parent-selector descendant-selector {
  declaration
}

//Example: <li><h4 class='destination'>Jackson Hole, Wyoming</h4></li>
li h4{
  color: gold;
}
```

### Multiple Selectors
```CSS
h5,li{
font-family: monospace;
}
```


### Example HTML&CSS
```html
<!DOCTYPE html>
<html>
  <head>
    <link href='https://fonts.googleapis.com/css?family=Roboto:400,300,500,100' rel='stylesheet' type='text/css'>
<link href="style.css" rel="stylesheet">
  </head>
  <body>
    <div class="header">
      <div class="container">
        <h1>Innovation Cloud</h1>
        <p>Connect your ideas globally</p>
        <a class="btn" href="#">Learn More</a>
      </div>
    </div>

    <div class="nav">
      <div class="container">
        <ul>
          <li>Register</li>
          <li>Schedule</li>
          <li>Sponsors</li>
          <li>About</li>
          <li>Contact</li>
        </ul>
      </div>
    </div>

    <div class="main">
      <div class="container">
        <img src="https://content.codecademy.com/projects/innovation-cloud/cloud.svg" height="128" width="196">
        <h2>The Innovation Cloud Conference</h2>
        <p>Connect with the best minds across a wide range of industries to share ideas and brainstorm new solutions to challenging problems.</p>
        <p>Hear industry leaders talk about what worked (and what didn't) so that you can save time on your most challenging projects.</p>
        <p>Learn about the latest research and technologies that you can use immediately to invent the future.</p>
      </div>
    </div>

    <div class="jumbotron">
      <div class="container">
        <h2>Stay Connected</h2>
        <p>Receive weekly insights from industry insiders.</p>
        <a class="btn" href="#">Join</a>
      </div>
    </div>

    <div class="footer">
      <div class="container">
        <p>&copy; Innovation Cloud Conference</p>
      </div>
    </div>
  </body>
</html>
```

### Example CSS

```CSS
html, body {
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Roboto', sans-serif;
  font-weight: 100;
}

.container {
  margin: 0 auto;
  max-width: 940px; 
  padding: 0 10px;
}

.header {
  background: url(https://content.codecademy.com/projects/innovation-cloud/bg.jpg) no-repeat center center; 
  background-size: cover;
  height: 800px;
  text-align: center; 
}

.header .container {
  position: relative;
  top: 200px;
}

.header h1 {
  color: #fff;
  line-height: 100px; 
  font-size: 80px;
  margin-top: 0;
  margin-bottom: 80px;
  text-transform: uppercase; 
}

@media (min-width:850px) {
  .header h1 {
    font-size: 120px;
  }
}

.header p {
  color: #fff;
  font-weight: 500;
  letter-spacing: 8px;
  margin-bottom: 40px;
  margin-top: 0;
  text-transform: uppercase; 
}

.btn {
  color: #fff;
  background: #000;
  padding: 10px 40px;
  text-decoration: none; 
  transition: background .5s; 
}

.nav { 
  background: #000;
  height: 80px; 
  width: 100%;
}

.nav ul {
  height: 80px;
  list-style: none;
  margin: 0 auto; 
  padding: 0;
}

.nav ul li {
  color: #fff;
  display: inline-block; 
  height: 80px;
  line-height: 80px; 
  list-style: none;
  padding: 0 10px;
  transition: background .5s; 
}

.btn:hover, .nav ul li:hover {
  background: #117bff;
  cursor: pointer; 
  transition: background .5s;  
}

.main .container {
  margin: 80px auto;
}

.main img {
  float: left;
  margin: 50px 80px 50px 0;
}

.jumbotron {
  background: url(https://content.codecademy.com/projects/innovation-cloud/jumbotron_bg.jpg) center center;
  background-size: cover;
  height: 600px; 
}

.jumbotron .container {
  position: relative;
  top: 220px;
}

.jumbotron h2 {
  color: #fff;
  text-align: right; 
}

.jumbotron p {
  color: #fff; 
  text-align: right; 
}

.jumbotron .btn {
  margin: 10px 0 0;
  float: right; 
}

.footer { 
  background: #000;
  height: 80px; 
  padding-bottom: 50px;
}

.footer p { 
  color: #fff;
  font-size: 14px;  
  height: 80px; 
  line-height: 80px;
  margin: 0;  
}

@media (max-width: 500px) {
  .header h1 {
    font-size: 50px;
    line-height: 64px;
  }

  .main, .jumbotron {
    padding: 0 30px;
  }

  .main img {
    width: 100%;
  }
}
```