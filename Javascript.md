# Javascript

[Structure](#structure)\
[Data](#data)\
[Console](#console)\
[Flow](#flow)



Confirmation box with OK / Cancel buttons

```javascript
if (confirm("This is a question")) {
    console.log("Alrighty then we're in business.")
} else {
    console.log("Fine then, we won't do the thing.")
}
```

Ternary operator
```javascript
let result = (a + b == 10 ? "equal 10" : "doesn't equal 10")
```

Arrow function
```javascript
let sum = (a, b) => a + b;
```

Alert
```javascript
alert("This is an IMPORTANT message")
```
Prompt box with imput
```javascript
prompt("Please enter your name", "example name")
```

Removes element(s) from array
```javascript
function removeFromArray(array, ...theArgs) {
    for (var i = 0; i < theArgs.length; i++) {
        if (array.includes(theArgs[i])) {
        array.splice(array.indexOf(theArgs[i]), 1)
        }   
    }
    return array 
}     
```
Function with default value
```javascript
let getScoreText = function(name, score = 0) {
    console.log(name)
    console.log(score)
}
```
Template Strings
```javascript
let name = 'Jen'

console.log(`Hey my name is ${name}!`)
```
Create an object
```javascript
let myBook = {
    title: '1984',
    author: 'George Orwell',
    pageCount: 326
}
```
Function the returns new object (ie return multiple properties)
```javascript
let getSummary = function (book) {
    return {
        summary: `${book.title} by ${book.author}`,
        pageCountSummary: `${book.title} is ${book.pageCount} pages long` 
    }
}
console.log(getSummary(myBook).pageCountSummary)
```
Array Methods
```javascript
console.log(notes.pop())
notes.push('My new note')

console.log(notes.shift())
notes.unshift('My new first note')

notes.splice(1, 2, 'This is the new second item', 'New Third Item')
```



