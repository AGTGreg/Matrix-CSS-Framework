Matrix-UI-Framework
===================

Matrix is a free and simple to use ui framework for responsive web pages.

How to install:
===============
1. Download the files to your computer.
2. Include the matrix-grid.css file in your page. 
   ie: 
   ```html 
   <link rel="stylesheet" type="text/css" media="screen" href="css/matrix-grid.css" />
   ```
3. Link to the latest jQuery. 
   ie: 
   ```html
   <script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
   ```
4. And last:  Matrix uses inline-blocks for the layout. So we need to remove the unwanted whitespace between them. Because there is no bulletproof method of removing whitespaces by using only css we need to add this script. You can write it in you head tag after the jQuery or in the end of your page. :
   ```javascript
   <script type="text/javascript">
       $(document).ready(function() {
           $('.matrix').contents().filter(function() {
             return this.nodeType == 3 && !/\S/.test(this.nodeValue);
           }).remove();
       });
   </script>
   ```
And you're done!
> Tip: It is a good practice to add a viewport meta tag with initial-scale=1.0 for good measure. Just put in the head tag of you document.
> ```html
> <meta name="viewport" content="width=device-width, initial-scale=1.0">
>```
