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
const getThingsDone = function(array) {
    return array.filter(function(each) {
        return each.completed
    })
}    console.log("Fine then, we won't do the thing.")
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
Create object with methods
```javascript
let person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName
  }
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
forEach with callback function - Iterates through array
```javascript
notes.forEach(function (item, index) {
    console.log(index)
    console.log(item)
})
```
indexOf - always use ===, not suitable for array of objects

findIndex - returns index of item that return (true)
```javascript
const index = notes.findIndex(function(each) {
    return each.title === 'Habits to work on'
})
```
array.filter - Returns array of items that match
```javascript
const getThingsDone = function(array) {
    return array.filter(function(each) {
        return each.completed
    })
}
```
Sort array of objects according to property
```javascript
const sortNotes = function(notes) {
    notes.sort(function(a, b) {
        if (a.title.toLowerCase() < b.title.toLowerCase()) {
            return -1
        } else if (b.title.toLowerCase() < a.title.toLowerCase()) {
            return 1
        } else {
            return 0
        }
    })
}
```

## HTML DOM
select a paragraph
```javascript
const parapgrah = document.querySelector('p')
```
select all paragraphs, save as list
```javascript
const paragraphs = document.querySelectorAll('p')
```
iterate through list of paragraphs, remove one that matches
```javascript
paragraphs.forEach(function (p) {
    if (p.textContent.toLowerCase().includes('cat')) {
        p.remove()
    }
})
```
append new elemend
```javascript
const newParagraph = document.createElement('p')
newParagraph.textContent = 'This is a new element from Javascript'
document.querySelector('body').appendChild(newParagraph)
```
add eventlistener to button
```javascript
document.querySelector('button').addEventListener('click', function(e) {
    console.log('Did this work?')
    console.log(e)
})
```
text input, real time character update
```javascript
document.querySelector('#search-text').addEventListener('input', function(e) {
    console.log(e.target.value)
})
```
clear div of html content
```javascript
document.querySelector('#notes').innerHTML = ''
```

Form
```html
<form id="name-form">
    <input type="text" placeholder="First name" name="firstName">
    <button>Submit</button>
</form>
```
```javascript
document.querySelector('#name-form').addEventListener('submit', function(e) {
    e.preventDefault()
    console.log(e.target.elements.firstName.value)
    e.target.elements.firstName.value = ''
})
```
Checkbox
```html
<label>
    <input id="for-fun" type="checkbox"> Check me for fun
</label>
```
```javascript
document.querySelector('#for-fun').addEventListener('change', function(e) {
    console.log(e.target.checked)
})
```
Dropdown
```html
<select id="filter-by">
    <option>Sort by last edited</option>
    <option>Sort by recently created</option>
    <option>Sort alphabetically</option>
</select>
```
```javascript
document.querySelector('#filter-by').addEventListener('change', function(e) {
    console.log(e.target.value)
})
```
CRUD local storage
```javascript
// (C) reate
localStorage.setItem('location', 'Newcastle NSW')
// (R) ead
console.log(localStorage.getItem('location'))
// (U) pdate
localStorage.setItem('location', 'Newcastle NSW')
// (D) elete
localStorage.removeItem('location')
localStorage.clear()  // Removes all
```
JSON - create javascript object, convert to JSON string and sent to storage, than retrieve it and change it back
```javascript
const userJSON = JSON.stringify(user)
localStorage.setItem('user', userJSON)

const newUserJSON = localStorage.getItem('user')
const newUser = JSON.parse(userJSON)
console.log(`${newUser.name} is ${newUser.age} years old.`)
```
