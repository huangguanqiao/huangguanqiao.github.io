---
layout:     post
title:    HTML Review
subtitle:   BY Guanqiao Huang
date:       2019-01-11
author:     HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - HTML
---

## INTRODUCTION TO HTML

- HTML stands for HyperText Markup Language and is used to create the structure and content of a webpage.
- Most HTML elements contain opening and closing tags with raw text or other HTML tags between them.
- HTML elements can be nested inside other elements. The enclosed element is the child of the enclosing parent element.
- Any visible content should be placed within the opening and closing <body> tags.
- Headings and sub-headings, `<h1>` to `<h6>` tags, are used to provide titles for sections of content.
- `<p>`, `<span>` and `<div>` tags specify text or blocks.
- The `<em>` and `<strong>` tags are used to emphasize text.
- Line breaks are created with the `<br>` tag.
- Ordered lists (`<ol>`) are numbered and unordered lists (`<ul>`) are bulleted.
- Images (`<img>`) and videos (`<video>`) can be added by linking to an existing source.

Flat tree and Structured Treee

## TML DOCUMENT STANDARDS
- The `<!DOCTYPE html>` declaration should always be the first line of code in your HTML files. This lets the browser know what version of HTML to expect.
- The `<html>` element will contain all of your HTML code.
- Information about the web page, like the title, belongs within the <head> of the page.
- You can add a title to your web page by using the `<title>` element, inside of the head.
- A webpage’s title appears in a browser’s tab.
- Anchor tags (`<a>`) are used to link to internal pages, external pages or content on the same page.
- You can create sections on a webpage and jump to them using `<a>` tags and adding ids to the elements you wish to jump to.
- Whitespace between HTML elements helps make code easier to read while not changing how elements appear in the browser.
- Indentation also helps make code easier to read. It makes parent-child relationships visible.
- Comments are written in HTML using the following syntax: `<!-- comment -->`.

### Example 1
```html
<!DOCTYPE html>
<html>

<head>
  <title>Brown Bears</title>
</head>

<body>
  <nav>
    <a href="./index.html">Brown Bear</a>
    <a href="./aboutme.html">About Me</a>
  </nav>
  <h1>The Brown Bear</h1>
  <nav>
    <ul>
      <li><a href="#introduction">Introduction</a></li>
      <li><a href="#habitat">Habitat</a></li>
      <li><a href="#media">Media</a></li>
    </ul>
  </nav>
  <div id="introduction">
    <h2>About Brown Bears</h2>
    <p>The brown bear (<em>Ursus arctos</em>) is native to parts of northern Eurasia and North America. Its conservation status is currently <strong>Least Concern</strong>.<br /><br /> There are many subspecies within the brown bear species, including the
      Atlas bear and the Himalayan brown bear.</p>
    <a href="https://en.wikipedia.org/wiki/Brown_bear" target="_blank">Learn More</a>
    <h3>Species</h3>
    <ul>
      <li>Arctos</li>
      <li>Collarus</li>
      <li>Horribilis</li>
      <li>Nelsoni (extinct)</li>
    </ul>
    <h3>Features</h3>
    <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
  </div>
  <div id="habitat">
    <h2>Habitat</h2>
    <h3>Countries with Large Brown Bear Populations</h3>
    <ol>
      <li>Russia</li>
      <li>United States</li>
      <li>Canada</li>
    </ol>
    <h3>Countries with Small Brown Bear Populations</h3>
    <p>Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.</p>
  </div>
  <div id="media">
    <h2>Media</h2>
    <img src="https://content.codecademy.com/courses/web-101/web101-image_brownbear.jpg" />
    <video src="https://content.codecademy.com/courses/freelance-1/unit-1/lesson-2/htmlcss1-vid_brown-bear.mp4" height="240" width="320" controls>Video not supported</video>
  </div>
</body>

</html>

```

### Example 2
```html
<!DOCTYPE html>
<html>
<head>
<title>Everyday with Isa</title>
  </head>

  <body>
      <a href="#contact"><img src="https://content.codecademy.com/courses/learn-html/elements-and-structure/profile.jpg"></a>
  <h3>by Isabelle Rodriguez | 1 day ago</h3>
<h1>“An Insider’s Guide to NYFW”</h1>
<img src="https://content.codecademy.com/courses/learn-html/elements-and-structure/image-one.jpeg">
<p>“<a href="https://en.wikipedia.org/wiki/New_York_Fashion_Week" target="_blank">NYFW</a> can be both amazingly fun & incredibly overwhelming, especially if you’ve never been. Luckily, I’m here to give you an insider’s guide and make your first show a pleasurable experience. By taking my tips and tricks, and following your gut, you’ll have an unforgettable experience!”</p>
<h2>“Getting Tickets & Picking the Shows”</h2>
<img src="https://content.codecademy.com/courses/learn-html/elements-and-structure/image-two.jpeg">
<p>“If you’re lucky or connected you can get an invite, sans the price tag. But I wasn’t so lucky or connected my first 2 years so I’m here to help you out. First, plan out which shows are most important to you and make a schedule and this is a biggie: SET A BUDGET. If you’re worrying about blowing your cash the whole time you won’t have fun. Then check out prices, days, and times and prioritize the designers you want to see most. Lastly, purchase your tickets and get excited!”</p>
<h2>“Dressing for the Shows”</h2>
<img src="https://content.codecademy.com/courses/learn-html/elements-and-structure/image-three.jpeg">
<p>“Always be true to your own sense of style, if you don’t you’ll be uncomfortable the whole time and it will show. Remember, NYFW is about expressing yourself and taking in what the designers have chosen to express through their new lines. Also it’s important to wear shoes you’ll be comfortable in all day. Obviously you want to look good, but you’ll be on your feet all day long, so be prepared.”</p>
  </body>
  

  <h4>Related Content</h4>
  <ul>
    <li>“How To Style Boyfriend Jeans”</li>
    <li>“When Print Is Too Much”</li>
    <li>“The Overalls Trend”</li>
    <li>“Fall’s It Color: Blush”</li>
  </ul>
  <div id="contact">
  <p><strong>email</strong>:isa@fashionblog.com | <strong>phone</strong>: 917-555-1098 | <strong>address</strong>: 371 284th St, New York, NY, 10001</p>
  </div>
</html>
```

## HTML TABLES
- The `<table>` element creates a table.
- The `<tr>` element adds rows to a table.
- To add data to a row, you can use the `<td>` element.
- Table headings clarify the meaning of data. Headings are added with the `<th>` element.
- Table data can span columns using the `colspan` attribute.
- Table data can span rows using the `rowspan` attribute.
- Tables can be split into three main sections: a head, a body, and a footer.
- A table’s head is created with the `<thead>` element.
- A table’s body is created with the `<tbody>` element.
- A table’s footer is created with the `<tfoot>` element.
- All the CSS properties you learned about in this course can be applied to tables and their data.

### Example 1
```html
<!DOCTYPE html>
<html>
<head>
  <title>Ship To It - Company Packing List</title>
  <link href="https://fonts.googleapis.com/css?family=Lato: 100,300,400,700|Luckiest+Guy|Oxygen:300,400" rel="stylesheet">
  <link href="style.css" type="text/css" rel="stylesheet">
</head>
<body>

  <ul class="navigation">
    <li><img src="https://content.codecademy.com/courses/web-101/unit-9/htmlcss1-img_logo-shiptoit.png" height="20px;"></li>
    <li class="active">Action List</li>
    <li>Profiles</li>
    <li>Settings</li>
  </ul>

  <div class="search">Search the table</div>
  
  <table>
    <thead>
    <tr>
      <th>Company Name</th>
      <th>Number of Items to Ship</th>
      <th>Next Action</th>
    </tr>
    </thead>
    <tbody>
    <tr>
      <td colspan="2">Adam's Greenworks</td>
      <td>14</td>
      <td>Package Items</td>
    </tr>
    <tr>
      <td rowspan="2">Davie's Burgers</td>
      <td>2</td>
      <td>Send Invoice</td>
    </tr>
    <tr>
      <td>Baker's Bike Shop</td>
      <td>3</td>
      <td>Send Invoice</td>
    </tr>
    <tr>
      <td>Miss Sally's Southern</td>
      <td>4</td>
      <td>Ship</td>
    </tr>
    <tr>
      <td>Summit Resort Rentals</td>
      <td>4</td>
      <td>Ship</td>
    </tr>
    <tr>
      <td>Strike Fitness</td>
      <td>1</td>
      <td>Enter Order</td>
    </tr>
    </tbody>

    <tfoot>
      <td>Total</td>
<td>28</td>
      </tfoot>
  </table>


</body>
</html>
```

### Example 2
```html
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <title>Aguillar Family Wine Festival</title>
  <link rel="stylesheet" type="text/css" href="reset.css" />
  <link rel="stylesheet" type="text/css" href="style.css" />
  <link href="https://fonts.googleapis.com/css?family=Oswald" rel="stylesheet">
</head>

<body>
  <header>
    <h1>Annual Aguillar Family Wine Festival</h1>
  </header>
  
  <div class="container">
  <table>
      <thead>
       
        <tr>
          <th colspan="2"> <h1>Wine Festival Schedule</h1></th>
        </tr>

        <tr>
          <th><h2>TIME</h2></th>
           <th><h2>EVENT</h2></th>
        </tr>
      </thead>

      <tbody>
        <tr>
          <td class="left"><h3>12:00 PM</h3></td>
           <td><h3>Welcome Reception</h3></td>
        </tr>
          <tr>
          <td class="left"><h3>01:00 PM</h3></td>
           <td><h3>Storytelling & Tasting</h3></td>
        </tr>
          <tr>
          <td class="left"><h3>02:00 PM</h3></td>
           <td><h3>Wine Luncheon</h3></td>
        </tr>
          <tr>
          <td class="left"><h3>03:00 PM</h3></td>
           <td><h3>Aguillar Family Wines</h3></td>
        </tr>
          <tr>
          <td class="left"><h3>04:00 PM</h3></td>
           <td><h3>Wine & Cheese Tasting</h3></td>
        </tr>
      </tbody>
  </table>
  </div>
  
  <footer>
    <h3>Contact</h3>
    <h3>Location</h3>
    <h3>Privacy Policy</h3>
  </footer>
</body>

</html>

```

## HTML FORMS

- The purpose of a <form> is to allow users to input information and send it.
- The `<form>`‘s action attribute determines where the form’s information goes.
- The `<form>`‘s method attribute determines how the information is sent and processed.
- To add fields for users to input information we use the `<input>` element and set the type attribute to a field of our choosing:
- Setting type to "text" creates a single row field for text input.
- Setting type to "password" creates a single row field that censors text input.
- Setting type to "number" creates a single row field for number input.
- Setting type to "range" creates a slider to select from a range of numbers.
- Setting type to "checkbox" creates a single checkbox which can be paired with other checkboxes.
- Setting type to "radio" creates a radio button that can be paired with other radio buttons.
- Setting type to "list" will pair the `<input>` with a `<datalist>` element if the id of both are the same.
- Setting type to "submit" creates a submit button.
- A `<select>` element is populated with <option> elements and renders a dropdown list selection.
- A `<datalist>` element is populated with <option> elements and works with an <input> to search through choices.
- A `<textarea>` element is a text input field that has a customizable area.
When a <form> is submitted, the name of the fields that accept input and the value of those fields are sent as name=value pairs.

### Example 1
```html
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <link rel="stylesheet" type="text/css" href="style.css">
    <link href="https://fonts.googleapis.com/css?family=Rubik" rel="stylesheet">
    <title>Password Input</title>
  </head>
  <body>
    <section id="overlay">
      <img src="https://content.codecademy.com/courses/web-101/unit-6/htmlcss1-img_burger-logo.svg" alt="Davie's Burgers Logo" id="logo">
      <hr>
      <form>
				<h1>Login to start creating a burger!</h1>
        <label for="username">Username:</label>
  			<input type="text" name="username" id="username">
        <br>
        <label for="user-pw">Password:</label>
        <!--Add your code below-->
				<input type="password" name="user-pw" id="user-pw">
      </form>
    </section>
  </body>
</html>
```

### Example 2
```html
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <link rel="stylesheet" type="text/css" href="style.css">
    <link href="https://fonts.googleapis.com/css?family=Rubik" rel="stylesheet">
    <title>Forms Review</title>
  </head>
  <body>
    <section id="overlay">
      <img src="https://content.codecademy.com/courses/web-101/unit-6/htmlcss1-img_burger-logo.svg" alt="Davie's Burgers Logo" id="logo">
      <hr>
      <form action="submission.html" method="POST">
				<h1>Create a burger!</h1>
        <section class="protein">
          <label for="patty">What type of protein would you like?</label>
    			<input type="text" name="patty" id="patty">
        </section>
        <hr>
        
        <section class="patties">
          <label for="amount">How many patties would you like?</label>
          <input type="number" name="amount" id="amount">
        </section>
        <hr>
        
        <section class="cooked">
          <label for="doneness">How do you want your patty cooked</label>
          <br>
          <span>Rare</span>
          <input type="range" name="doneness" id="doneness" value="3" min="1" max="5">
          <span>Well-Done</span>
        </section>
        <hr>
        
        <section class="toppings">
          <span>What toppings would you like?</span>
          <br>
          <input type="checkbox" name="topping" id="lettuce" value="lettuce">
          <label for="lettuce">Lettuce</label>
          <input type="checkbox" name="topping" id="tomato" value="tomato">
          <label for="tomato">Tomato</label>
          <input type="checkbox" name="topping" id="onion" value="onion">
          <label for="onion">Onion</label>
        </section>
        <hr>
        
        <section class="cheesy">
          <span>Would you like to add cheese?</span>
          <br>
          <input type="radio" name="cheese" id="yes" value="yes">
          <label for="yes">Yes</label>
          <input type="radio" name="cheese" id="no" value="yes">
          <label for="no">No</label>
        </section>
        <hr>
       
        <section class="bun-type">
          <label for="bun">What type of bun would you like?</label>
          <select name="bun" id="bun">
            <option value="sesame">Sesame</option>
            <option value="potatoe">Potato</option>
            <option value="pretzel">Pretzel</option>
          </select>
        </section>
        <hr>
        
        <section class="sauce-selection">
          <label for="sauce">What type of sauce would you like?</label>
          <input list="sauces" id="sauce" name="sauce">
          <datalist id="sauces">
            <option value="ketchup"></option>
            <option value="mayo"></option>
            <option value="mustard"></option>
          </datalist>
        </section>
        <hr>
        <section class="extra-info">
          <label for="extra">Anything else you want to add?</label>
          <br>
          <textarea id="extra" name="extra" rows="3" cols="40"></textarea>
        </section>
        <hr>

        <section class="submission">
          <input type="submit" value="Submit">
        </section>
      </form>
    </section>
  </body>
</html>

```