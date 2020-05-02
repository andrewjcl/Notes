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
String template
```javascript
let name = 'Jen'

console.log(`Hey my name is ${name}!`)
```
