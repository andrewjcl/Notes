# HTML

[Structure](#structure)\
[Data](#data)\
[Console](#console)\
[Flow](#flow)

```
https://learn.freecodecamp.org/responsive-web-design/basic-html-and-html5/say-hello-to-html-elements/
```
## Basic Tags


```html
<!-- This is a comment -->
<!DOCTYPE html>
<html>
  <head>  <!-- Head displays meta data information, title bar, meta, style etc. -->
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
