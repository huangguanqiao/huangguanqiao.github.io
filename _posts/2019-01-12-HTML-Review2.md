---
layout:     post
title:    HTML Review2
subtitle:   BY Guanqiao Huang
date:       2019-01-12
author:     HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - HTML
---
## SEMANTIC HTML
- Semantic HTML introduces meaning to a page through specific elements that provide context as to what is in between the tags.
- Semantic HTML is a modern standard and makes a website accessible for people who use screen readers to translate the webpage and improves your website’s SEO.
- `<header>`, `<nav>` , `<main>` and `<footer>` create the basic structure of the webpage.
- `<section>` defines elements in a document, such as chapters, headings, or any other area of the document with the same theme.
- `<article>` holds content that makes sense on its own such as articles, blogs, comments, etc.
- `<aside>` contains information that is related to the main content, but not required in order to understand the dominant information.
- `<figure>` encapsulates all types of media.
- `<figcaption>` is used to describe the media in `<figure>`.
- `<figcaption>` is used to insert text related to the content in the `<figure>` such as a description.
- `<video>`, `<embed>`, and `<audio>` elements are used for media files.
- Embed can be used for files or external links such as a video from a different website.

### Example 1
```html
<!DOCTYPE html>
<html>

<head>
    <link rel="stylesheet" type="text/css" href="style.css">
</head>

<body>
    <header>
        <h1>Navigational Links</h1>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#posts">Posts</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section>
            <article>
                <h2>Facts About Dogs</h2>
                <p>
                    Dogs have a sense of time. It's been proven that they know the difference between a hour and five.
                    If conditioned to, they can predict future events, such as regular walk times.
                </p>
            </article>
            <aside>
                <p>A study was conducted on dogs being away from their owners for varying hours and the studies show
                    that dogs who were away from their owners the longest showed the greatest amount of affection!
                </p>
            </aside>
        </section>
        <figure>
            <img src="https://content.codecademy.com/courses/SemanticHTML/dogimage.jpeg" />
            <figcaption>A cute dog.</figcaption>
        </figure>
        <audio controls>
            <source src="https://content.codecademy.com/courses/SemanticHTML/dogBarking.mp3" type="audio/mp3">
        </audio>
        <video src="https://content.codecademy.com/courses/SemanticHTML/dog-video.mp4" controls>
        </video>
        <embed src="https://content.codecademy.com/courses/SemanticHTML/dog-on-beach.gif" />

    </main>

    <footer>
        <p>Contact me at +1 234 567 8910 </p>
    </footer>

</body>

</html>
```

### Example 2
```html
<!DOCTYPE html>
<html>

<head>
    <link rel="stylesheet" href="style.css">
</head>

<body>
    <nav>
        <ul>
            <li><a href="">Blog</a></li>
            <li><a href="">Media</a></li>
            <li><a href="">About</a></li>
        </ul>
    </nav>

    <header>
        <h1>New York City</h1>
    </header>

    <main>
        <section>
            <article>
                <p>New York City is made up of five boroughs which include Queens, Manhattan, Brooklyn, the Bronx, and
                    Staten Island. The city is the home of approximately 8 million people. In 1876, France gifted the
                    City of New York what is known as the Statue of Liberty, which is currently located on Ellis Island
                    commonly visited by tourists. However, it took 10 years to assemble and therefore wasn’t unveiled
                    until 1886. Another tourist destination is Times Square. Times Square is commonly known for the big
                    buildings, Broadway shows, and bright neon signs. This famous location was named after The New York
                    Times after the Times moved to that location. Prior to that, it was named Longacre Square. New York
                    City is also known for its bridges that connect the boroughs and allow ease of transportation.</p>
            </article>
        </section>

        <figure>
            <img src="https://content.codecademy.com/courses/Semantic%20HTML/statue-of-liberty.jpeg">
        </figure>
        <figcaption>This is the Statue of Liberty, a popular tourist attraction located on Ellis Island.</figcaption>

        <aside>
            <p>New York City is very popular for the variety of great food it has. Some of the top food items in NYC
                include:</p>
            <ol>
                <li>Pizza</li>
                <li>Bagels</li>
                <li>Burgers and Sandwiches</li>
                <li>Ramen</li>
                <li>Tacos</li>
                <li>Pasta</li>
                <li>Desserts</li>
            </ol>
        </aside>

        <section>
            <article>
                <h2>The Scenery in NYC</h2>
                <p>While the view in the city is beautiful, the sounds are not as lovely. Below you'll see an example of
                    the view and the sounds you'll deal with in NYC on a daily basis.</p>
            </article>
            <video src="https://content.codecademy.com/courses/Semantic%20HTML/nyc-skyline-timelapse.mp4"
                controls></video>
            <embed src="https://content.codecademy.com/courses/Semantic%20HTML/nyc-skyline.jpeg">

            <audio src="https://content.codecademy.com/courses/Semantic%20HTML/nyc-sounds.mov" controls></audio>
        </section>

    </main>
    <footer id="about">
        <p>Posted by:Guanqiao Huang</p>
        <p>Contact information: huangguanqiao@foxmail.com</p>
    </footer>



</body>

</html>
```