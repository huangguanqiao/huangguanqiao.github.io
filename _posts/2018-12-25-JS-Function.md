---
layout:     post
title:     JavaScript Function
subtitle:   BY Guanqiao Huang
date:       2018-12-25
author:     HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - JavaScript
---
## Default Parameters
- Default parameters allow parameters to have a predetermined value in case there is no argument passed into the function or if the argument is undefined when called.

### Example 1

```Javascript
function greeting (name = 'stranger') {
  console.log(`Hello, ${name}!`)
}
 
greeting('Nick') // Output: Hello, Nick!
greeting() // Output: Hello, stranger!
```
### Example 2
```Javascript
function makeShoppingList(item1='milk', item2='bread', item3='eggs'){
  console.log(`Remember to buy ${item1}`);
  console.log(`Remember to buy ${item2}`);
  console.log(`Remember to buy ${item3}`);
}
```

## Return
```Javascript
function rectangleArea(width, height) {
  if (width < 0 || height < 0) {
    return 'You need positive integers to calculate area!';
  }
  return width * height;
}
```

## Helper Functions
```Javascript
function monitorCount(rows, columns){
  return rows*columns;
}

const numOfMonitors = monitorCount(5,4);
console.log(numOfMonitors);
```

```Javascript
function monitorCount(rows, columns) {
  return rows * columns;
}

function costOfMonitors(rows,columns){
return monitorCount(rows, columns)*200;
}

const totalCost = costOfMonitors(5,4);
console.log(totalCost);
```

## Function Expressions
- A function with no name is called an anonymous function. A function expression is often stored in a variable in order to refer to it.
```Javascript
const plantNeedsWater = function(day){
 if(day === 'Wednesday'){
   return true;
 }
 else{
   return false;
 }
};

console.log(plantNeedsWater('Tuesday'));
```

## Arrow Functions
```Javascript
const plantNeedsWater = (day) => {
  if (day === 'Wednesday') {
    return true;
  } else {
    return false;
  }
};
```

## Concise Body Arrow Function $ Implicit return
```Javascript
//Normal way
const plantNeedsWater = (day) => {
  return day === 'Wednesday' ? true : false;
};
```

```Javascript
//One line
const plantNeedsWater = day => day === 'Wednesday' ? true : false;
```

# Practice
## Rock, Paper, or Scissors
### User Choice
```Javascript
//Example 1.1 One line (Best one line)
const getUserChoice = userInput => (userInput = userInput.toLowerCase(), (userInput === 'paper')||(userInput ==='rock')||(userInput ==='scissors') ? userInput : console.log('error'));
```


```Javascript
//Example 1.0 One line
const getUserChoice = userInput => (userInput.toLowerCase() === 'paper')||(userInput.toLowerCase() ==='rock')||(userInput.toLowerCase() ==='scissors') ? userInput.toLowerCase() : console.log('error');
```

```Javascript
//Example 2.1 One line
const getUserChoice2 = userInput => (userInput = userInput.toLowerCase(), (userInput === 'paper') ? userInput : (userInput === 'rock' ) ? userInput : (userInput === 'scissors') ? userInput : console.log('error'));
```

```Javascript
//Example 2.0 One line
//Way: var variable = (condition) ? (true block) : ((condition2) ? (true block2) : (else block2))

const getUserChoice2 = userInput => userInput.toLowerCase() === 'paper' ? userInput.toLowerCase() : userInput.toLowerCase() === 'rock'  ? userInput.toLowerCase() : userInput.toLowerCase() === 'scissors' ? userInput.toLowerCase(): console.log('error');
```

```Javascript
//Example 3 Array Function
const getUserChoice3 = userInput =>{
  userInput = userInput.toLowerCase();
  if(userInput==='paper'||userInput==='rock'||userInput==='scissors'){
    return userInput;
  }
  else{
    console.log('error');
  }
}
```

```Javascript
//Example 3 Array Function + Switch
const getUserChoice3 = userInput =>{
  userInput = userInput.toLowerCase();
 switch (userInput){
   case 'rock':
   return userInput;
   break;
   case 'paper':
   return userInput;
   break;
   case 'scissors':
   return userInput;
   break;
   default:
    console.log('error');
  }
}
```

```Javascript
//Example 4 My standard  style
function getUserChoice4(userInput){
  userInput = userInput.toLowerCase();
  if(userInput==='paper'||userInput==='rock'||userInput==='scissors'){
    return userInput;
  }
  else{
    console.log('error');
  }
}
```

### Computer Choice
```Javascript
//Normal way
function getComputerChoice (){
  let num = Math.floor(Math.random()*3);
  switch(num){
    case 0:
    return 'rock';
    break;
    case 1:
    return 'paper';
    break;
    case 2:
    return 'scissors';
    break;
    deafult:
    break;
  }
}
```

```Javascript
const getComputerChoice = () => {
    let num = Math.floor(Math.random()*3);
  switch(num){
    case 0:
    return 'rock';
    break;
    case 1:
    return 'paper';
    break;
    case 2:
    return 'scissors';
    break;
    deafult:
    break;
  }
}
```

```Javascript
const getComputerChoice = () => {
  let num = Math.floor(Math.random()*3); 
  if (num === 0) {
    return 'rock';
  } else if
  (num === 1) {
    return 'paper';
  } else if
  (num === 2) {
    return 'scissors';
  } 
  }
  ```

  ### Whole Games
  ```Javascript
  const getUserChoice = userInput => (userInput = userInput.toLowerCase(), (userInput === 'paper')||(userInput ==='rock')||(userInput ==='scissors') ? userInput : console.log('error'));

const getComputerChoice = () => {
    let num = Math.floor(Math.random()*3);
  switch(num){
    case 0:
    return 'rock';
    break;
    case 1:
    return 'paper';
    break;
    case 2:
    return 'scissors';
    break;
    deafult:
    break;
  }
}

const determineWinner = (userChoice, computerChoice) => {
  if(userChoice === computerChoice){
    return "Game was a tie";
  }
 else{
    if(userChoice === 'rock'){
    if(computerChoice === 'paper'){
      return "Computer Won";
    }
    else{
      return "User Won";
    }
  }
  else if(userChoice === 'paper'){
    if(computerChoice === 'rock'){
      return "User Won";
    }
    else{
      return "Computer Won";
    }
  }
  else{
    if(computerChoice === 'rock'){
      return "Computer Won";
    }
    else{
      return "User Won";
    }
  }
 }

}

const playGame = () => {
  let userChoice = getUserChoice('roCK');
  let computerChoice = getComputerChoice();
  console.log(userChoice + '<-->' + computerChoice);
  console.log(determineWinner(userChoice, computerChoice));
}

playGame();
```


Concise body syntax (with one parameter) does not use parentheses, curly braces, or the return keyword.