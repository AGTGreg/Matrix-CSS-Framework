Matrix-UI-Framework
===================

Matrix is a free and simple to use ui framework for responsive web pages.

> For now there's only the grid system. More features are planned and will be added in the future.

The Matrix Grid system makes it easy to create responsive layouts for web pages the right way. Matrix uses inline-blocks instead of floating divs. All blocks are centered by default so you can center elements in you page with ease. 

You can check the sample html document included to see how it works.
Or you can just keep reading ;)

How to install:
===============
**Step 1**: Download the files to your computer.

**Step 2**: Include the matrix-grid.css file in your page. ie: 
```html
   <link rel="stylesheet" type="text/css" media="screen" href="css/matrix-grid.css" />
```

**Step 3**: Link to the latest jQuery. ie: 
```html
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
```

**Step 4**: And last:  Matrix uses inline-blocks for the layout. So we need to remove the unwanted whitespace between them. Because there is no bulletproof method of removing whitespaces by using only css we need to add this script. You can write it in you head tag after the jQuery or in the end of your page. :
```javascript
<script type="text/javascript">
      $(document).ready(function() {
          $('.matrix').contents().filter(function() {
            return this.nodeType == 3 && !/\S/.test(this.nodeValue);
          }).remove();
      });
</script>
```

**And you're done!**

> Tip: It is a good practice to add a viewport meta tag with initial-scale=1.0 for good measure. Just put in the head tag of you document.
> ```html
> <meta name="viewport" content="width=device-width, initial-scale=1.0">
>```

