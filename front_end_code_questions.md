## Code analysis / quiz

Order the following CSS selectors by specificity
```css
p {}
#special {}
.selected {}
div p {}
.red .green .blah {}
```

Consider the code snippet below. If there are 5 `<div>` elements on the page, what will be the difference between the start and end times displayed?
```js
function getMinsSecs() {
  var dt = new Date();
  return dt.getMinutes()+":"+dt.getSeconds();
}

$( "input" ).on( "click", function() {
  $( "p" ).append( "Start time: " + getMinsSecs() + "<br />" );
  $( "div" ).each(function( i ) {
    $( this ).fadeOut( 1000 * ( i * 2 ) );
  });
  $( "div" ).promise().done(function() {
    $( "p" ).append( "End time: " + getMinsSecs() + "<br />" );
  });
});
```

- Explain what the following code does:
```js
$( "div" ).css( "width", "300px" ).add( "p" ).css( "background-color", "blue" );
```

Which of the two lines of code below is more efficient? Explain your answer.
```js
document.getElementById( "logo" );
```
or
```js
$( "#logo" );
```

## Code Challenges

Write code in jQuery to animate the `#expander` div, expanding it from 100 x 100 pixels to 200 x 200 pixels over the course of three seconds.

Build an HTML page with a circle that is centered both horizontally and vertically, using only CSS.

Following questions taken from http://www.toptal.com/jquery/interview-questions

Explain what the following code will do:
```js
$( "div#first, div.first, ol#items > [name$='first']" )
```

The code below is for an application that requires defining a click handler for all buttons on the page, including those buttons that may be added later dynamically. What is wrong with this code, and how can it be fixed to work properly even with buttons that are added later dynamically?
```js
// define the click handler for all buttons
$( "button" ).bind( "click", function() {
    alert( "Button Clicked!" )
});

/* ... some time later ... */

// dynamically add another button to the page
$( "html" ).append( "<button>Click Alert!</button>" );
```

Explain to me what's going on in this CSS selector:

```css
[role=navigation] > ul a:not([href^=mailto]) {

}
```

Write a function that validates a form entry.

Select an element on the page and change the font size with vanilla JavaScript.
