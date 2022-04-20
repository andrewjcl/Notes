# HTML / CSS

[Structure](#structure)\
[Data](#data)\
[Console](#console)\
[Flow](#flow)

```
https://learn.freecodecamp.org/responsive-web-design/basic-html-and-html5/say-hello-to-html-elements/
```
## CSS ##

CSS stands for Cascading Style Sheets. It is a style sheet language used for describing the presentation of a document
written in a markup language such as HTML. CSS is designed to enable the separation of presentation and content, including
layout, colours and fonts. Many webpages can share the same CSS file, improving consistency and easing workload. It also
means a browser can cache the CSS file on one page and then retreive that cache for all the pages on the site.

CSS can be applied to a document in three ways.

* Inline - by using the `style` attribute inside HTML elements
* Internal - by using a `<style>` element in the `<head>` section of a HTML page
* External - by using a `<link>` element to link an external CSS file

Generally external linking is preferred, however while learning it is common to use the first two styles for ease of demonstration.

```html
<h2 style="color: red;">This is my Heading</h2>   <!-- Changing the colour of text via inline style -->  

<!-- A style block placed in the head of a html document applies styles to the entire document -->
<style>

  /* A border must have a "border-style* to work */
  .green-border {
    border-color: green;
    border-width: 10px;
    border-style: solid;
  }
  
  h2 { 
    color: blue;
  }
  
  p {
    font-size: 16px;
    font-family: "Lobster", monospace;  /* Attempting to use google Lobster font, degrade to monospace if unable */
  }
  
  /* Creating a CSS class allows us to style any element given the class attribute */
  .red-text {
    color: red;
  }
</style>
```
Three properties control the amount of space that surrounds each HTML element

```padding``` controls the amount of space between the element's content and its border  
```padding: 20px 40px 20px 40px;``` 1 line element padding - TOP, RIGHT, BOTTOM, LEFT  
```margin``` controls the amount of space between an element's border and its surrounding elements


## HTML ##

```html
<!-- This is a comment -->
<!DOCTYPE html>
<html>
  <head>  <!-- Head displays meta data information, title bar, meta, style, links (CSS/JS) etc. -->
    <!-- Link that imports a google web font -->
    <link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
    <title> Title is what shows in the window tab </title>
  </head>
  <body> <!-- Body is for all content to be rendered on the page -->
    <h1>Heading</h1>
    <p>This is my first paragraph of text</p>
    
  </body>
</html>
<h1>This is a heading</h1>                                           <!-- Can use numbers 1 through to 6  each
                                                                          in progressively smaller fonts-->

<main>                                                               <!-- the main tags helps search engines find 
                                                                          the main content of your page -->
<p>This is a paragraph</p>
<img src="http://www.images.com/image.jpg" alt="Alt text goes here"> <!-- Inserting an image -->
<a href="www.google.com">This is the link to google</a>              <!-- Anchor 
                                                                          target="_blank" attribute causes link
                                                                          to open in new tab -->
</main>
<footer id="footer">This is my footer</footer>
<a href="#footer">Jump</a>                                           <!-- Anchor with ref to jump to id tag -->
<ul>                                                                 <!-- Unordered List -->
  <li>cat nip</li>
  <li>laser pointers</li>
  <li>lasagna</li>
</ul>
<p>Top 3 things cats hate:</p>
<ol>                                                                 <!-- Ordered List -->
  <li>flea treatment</li>
  <li>thunder</li>
  <li>other cats</li>
</ol>

<!-- A form is a container element for input elements. When a submit button in the form is clicked,
     the form data is sent to the form-handler file, specified by action attribute in opening form tag -->
<form action="/submit-cat-photo">                               
  <input type="text" placeholder="cat photo URL">
  <!-- Radio Buttons - grouped with name attribute so only 1 can be active at a time --> 
  <label><input id="indoor" value = "indoor" type="radio" name="indoor-outdoor"> Indoor</label>   
  <label><input id="outdoor" value = "outdoor" type="radio" name="indoor-outdoor"> Outdoor</label>  
</form>
```
