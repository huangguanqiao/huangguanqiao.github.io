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

## XHR POST Requests
```JS
const xhr = new XMLHttpRequest();
const url = 'https://api-to-call.com/endpoint';
const data = JSON.stringify({id: 200});
xhr.responseType = 'json';

xhr.onreadystatechange = () =>{
  console.log("xhr.readyState: "+ xhr.readyState);
  console.log("XMLHttpRequest.DONE: "+ XMLHttpRequest.DONE);
  if(xhr.readyState === XMLHttpRequest.DONE){
    return xhr.response;
  }
};

xhr.open('POST', url);
xhr.send(data);

```

### XHR Post Requests III
[Rebrandly URL Shortener API](https://www.codecademy.com/articles/rebrandly-signup)
API: 3edd33d3a613479483aab7b1869a49f3

```JS
// Information to reach API
//const apiKey = '<Your API Key>';
const url = 'https://api.rebrandly.com/v1/links';
const apiKey = "3edd33d3a613479483aab7b1869a49f3";
// Some page elements
const inputField = document.querySelector('#input');
const shortenButton = document.querySelector('#shorten');
const responseField = document.querySelector('#responseField');

// AJAX functions
const shortenUrl = () => {
  const urlToShorten = inputField.value;
  const data = JSON.stringify({destination: urlToShorten});
  const xhr = new XMLHttpRequest();
  xhr.responseType = 'json';
  xhr.onreadystatechange = () =>{
      if (xhr.readyState === XMLHttpRequest.DONE) {
      renderResponse(xhr.response);
    }
  };

  xhr.open('POST', url);
  xhr.setRequestHeader('Content-type', 'application/json');
  xhr.setRequestHeader('apikey', apiKey);
  xhr.send(data);
};


// Clear page and call AJAX functions
const displayShortUrl = (event) => {
  event.preventDefault();
  while(responseField.firstChild){
    responseField.removeChild(responseField.firstChild);
  }
  shortenUrl();
}

shortenButton.addEventListener('click', displayShortUrl);

```

## Review Requests I
- JavaScript is the language of the web because of its asynchronous capabilities. AJAX, which stands for Asynchronous JavaScript and XML, is a set of tools that are used together to take advantage of JavaScript’s asynchronous capabilities.

- There are many HTTP request methods, two of which are GET and POST.

- GET requests only request information from other sources.

- POST methods can introduce new information to other sources in addition to requesting it.

- GET requests can be written using an XMLHttpRequest object and vanilla JavaScript.

- POST requests can also be written using an XMLHttpRequest object and vanilla JavaScript.

- Writing GET and POST requests with XHR objects and vanilla JavaScript requires constructing the XHR object using new, setting the responseType, creating a function that will handle the response object, and opening and sending the request.

- To add a query string to a URL endpoint you can use ? and include a parameter.

- To provide additional parameters, use & and then include a key-value pair, joined by =.

- Determining how to correctly write the requests and how to properly implement them requires carefully reading the documentation of the API with which you’re working.
- The & character will separate parameters and allow you to add more parameters to the query string.
- query string, It provides additional information to the API in the URL.
- onreadystatechange is a(n) event handler

## fetch() GET Requests II
```JS
fetch('https://api-to-call.com/endpoint')
.then((response)=>{
  if(response.ok){
    return response.json();
  }
  throw new Error('Request failed!');
},(networkError) => {
  console.log(networkError.message);
})
.then((jsonResponse)=>{
  return jsonResponse;
});
```

## fetch() GET Requests III
```JS
// Information to reach API
const url = 'https://api.datamuse.com/words';
const queryParams = '?sl=';

// Selects page elements
const inputField = document.querySelector('#input');
const submit = document.querySelector('#submit');
const responseField = document.querySelector('#responseField');

// AJAX function
const getSuggestions = () => {
  const wordQuery = inputField.value;
  const endpoint = `${url}${queryParams}${wordQuery}`;
  
  fetch(endpoint, {cache: 'no-cache'}).then(response => {
    if (response.ok) {
      return response.json();
    }
    throw new Error('Request failed!');
  }, networkError => {
    console.log(networkError.message)
  }).then(jsonResponse=>{
   // renderRawResponse(jsonResponse);
   renderResponse(jsonResponse);
  })
}

// Clears previous results and display results to webpage
const displaySuggestions = (event) => {
  event.preventDefault();
  while(responseField.firstChild){
    responseField.removeChild(responseField.firstChild);
  }
  getSuggestions();
};

submit.addEventListener('click', displaySuggestions);
```

## fetch() POST Requests II
```JS
fetch('https://api-to-call.com/endpoint',{
  method: 'POST',
  body: JSON.stringify({id: '200'})
}).then((response)=>{
  if(response.ok){
    return response.json();
  }
  throw new Error('Request failed!');
}, networkError => console.log(networkError.message))
.then(jsonResponse=>{
  return jsonResponse;
});
```

## fetch() POST Requests V
```JS
// Information to reach API
const apiKey = '3edd33d3a613479483aab7b1869a49f3';
const url = 'https://api.rebrandly.com/v1/links';

// Some page elements
const inputField = document.querySelector('#input');
const shortenButton = document.querySelector('#shorten');
const responseField = document.querySelector('#responseField');

// AJAX functions
const shortenUrl = () => {
  const urlToShorten = inputField.value;
  const data = JSON.stringify({destination: urlToShorten});
  fetch(url,{
    method: 'POST',
     headers: {
        'Content-type': 'application/json',
        'apikey': apiKey
      },
      body: data
  }).then((response)=>{
  if(response.ok){
    //renderJsonResponse(response);
    return response.json();
  }
  throw new Error('Request failed!');
}, (networkError) => console.log(networkError.message))
.then(jsonResponse => {
  //renderRawResponse(jsonResponse);
  renderResponse(jsonResponse);
});
};

// Clear page and call AJAX functions
const displayShortUrl = (event) => {
  event.preventDefault();
  while(responseField.firstChild){
    responseField.removeChild(responseField.firstChild)
  }
  shortenUrl();
}

shortenButton.addEventListener('click', displayShortUrl);
```

## fetch() Post Requests III
[Rebrandly API](https://developers.rebrandly.com/)
[Codecademy Articles: Rebrandly URL Shortener API.](https://www.codecademy.com/articles/rebrandly-signup)

## async GET Requests II
```JS
const getData = async()=>{
  try{
    const response = await fetch('https://api-to-call.com/endpoint');
    if(response.ok){
      const jsonResponse = await response.json();
    return jsonResponse;
    }
    throw new Error('Request failed!');
  } catch(error){
    console.log(error);
  }
}
```

## async GET Requests III
```JS
// Information to reach API
const url = 'https://api.datamuse.com/words?';
const queryParams = 'rel_jja=';


// Selecting page elements
const inputField = document.querySelector('#input');
const submit = document.querySelector('#submit');
const responseField = document.querySelector('#responseField');

// AJAX function
// Code goes here
const getSuggestions = async()=>{
  const wordQuery = inputField.value;
  const endpoint = `${url}${queryParams}${wordQuery}`;

  try{
    const response = await fetch(endpoint,{cache: 'no-cache'});
    if(response.ok){
      const jsonResponse = await response.json();
      //renderRawResponse(jsonResponse);
      renderResponse(jsonResponse);
    //return jsonResponse;
    }
    throw new Error('Request failed!');
  } catch(error){
    console.log(error);
  }
}

// Clear previous results and display results to webpage
const displaySuggestions = (event) => {
  event.preventDefault();
  while(responseField.firstChild){
    responseField.removeChild(responseField.firstChild)
  }
  getSuggestions();
}

submit.addEventListener('click', displaySuggestions);

```

## async POST Requests
```JS
const getData = async() =>{
  try{
    const response = await fetch('https://api-to-call.com/endpoint',{
        method: 'POST',
        body: JSON.stringify({id:200})
    });
    if(response.ok){
      const jsonResponse = await response.json();
    return jsonResponse;
    }
    throw new Error('Request failed!');
  }catch(error){
    console.log(error);
  }
}
```
## async POST Requests III
[async POST Requests III](https://www.codecademy.com/workspaces/61fa725d4ad323964b6fe149)

## Review Requests
- GET and POST requests can be created a variety of ways.

- Use AJAX to asynchronously request data from APIs. fetch() and async/await are new functionalities developed in ES6 (promises) and ES8 respectively.

- Promises are a new type of JavaScript object that represent data that will eventually be returned from a request.

- fetch() is a web API that can be used to create requests. fetch() will return promises.

- We can chain .then() methods to handle promises returned by fetch().

- The .json() method converts a returned promise to a JSON object.

- async is a keyword that is used to create functions that will return promises.

- await is a keyword that is used to tell a program to continue moving through the message queue while a promise resolves.

- await can only be used within functions declared with async.

## Wanderlust Project
[Wanderlust Demo](https://content.codecademy.com/courses/intermediate-javascript-requests/wanderlust/wanderlust-v3/index.html)
[Wanderlust Github](https://github.com/RahimGuerfi/Wanderlust)

## Links
[JS Diagram XHR](https://content.codecademy.com/courses/intermediate-javascript-requests/diagrams/XHR%20GET%20diagram.svg)
[XML introduction](https://developer.mozilla.org/en-US/docs/Web/XML/XML_introduction)
[Datamuse](https://www.datamuse.com/api/)
[XHR GET Requests III](https://www.codecademy.com/workspaces/61f8e7c48f6c970a7a049534)
[XHR POST diagram](https://content.codecademy.com/courses/intermediate-javascript-requests/diagrams/XHR%20POST%20diagram.svg)
[fetch() GET diagram](https://content.codecademy.com/courses/intermediate-javascript-requests/diagrams/fetch%20GET%20diagram.svg)
[fetch() POST diagram](https://content.codecademy.com/courses/intermediate-javascript-requests/diagrams/fetch%20POST%20diagram.svg)
[fetch() POST Requests V](https://www.codecademy.com/workspaces/61fa34224ad323964b6f91cb)
[async/await GET diagram](https://content.codecademy.com/courses/intermediate-javascript-requests/diagrams/async%20await%20GET%20diagram.svg)
[async/await POST diagram](https://content.codecademy.com/courses/intermediate-javascript-requests/diagrams/async%20await%20POST%20diagram.svg)
