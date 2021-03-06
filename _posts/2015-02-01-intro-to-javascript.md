---
title: Introduction to JavaScript and jQuery
---
---
layout: post
title: jQuery Basics
language: jquery
---
# Why This is Important:
The jQuery library makes tons of things we’d want to do on the web with JavaScript a breeze!

# Benefits of jQuery:
+ finding particular elements on the page
+ adding and removing elements
+ changing content on the fly
+ triggering an action when a user clicks a particular element
+ triggering an action when a user types on the keyboard
+ hiding and showing elements
+ changing the style of elements on the fly
+ getting data from a server
+ sending data to a server

If you are looking for something in particular, check out the [jQuery Cheatsheet](http://oscarotero.com/jquery/) and look for what you want to do. We'll go over the main things you can do now, but don't worry about memorizing - you'll always be able to look up the syntax when you need to.

# jQuery - Selection and the DOM
In order to do anything with jQuery, we first need to be able to navigate the DOM. In the Twitter example, we saw that we could select all elements that match a certain criteria with the $() method.

Some examples:


|CSS          |jQuery           |Selected        |
|---          |---              |---             |
|p            |$('p')           |All the paragraph elements|
|div          |$('div')         |All the div elements|
|.button      |$('.button')     |All elements with class=”button”|
|#headline    |$('#headline')   |The element with id=”headline”|
|.code strong |$('.code strong')|all of the strong elements with parent elements with the class="code"|
|header nav li.home|$('header nav.home')|All the li elements inside navs inside headers with the class home'|

<br>

# More Selection
There’s lots of ways to select elements, and pretty much any kind of element selection problem is easy with jQuery - if you can find the right method! If you have the time, check out the other methods on the [cheatsheet](http://oscarotero.com/jquery/). See if you can figure out what they do, and when you might need them.

# Adding and removing elements
Now that we know how to select elements and get around the DOM, let’s check out some of the cool things we can do!

Say you want a user to be able to add and remove items on a list - you don’t want to send a whole new HTML document from the server every time they do! Instead, you can use jQuery to add an element dynamically.

```
$('#my_list').append("<li>New element</li>")
```

And to remove an element:

```
$('#elementToRemove').remove()
```

The cheatsheet has lots more ways to add and remove elements. How would you add an element around a group of elements? How about removing an element without removing the elements inside it?

# jQuery and CSS
jQuery doesn’t just work to modify HTML - it also works to change the style of a page! Any kind of css that you might want to add, you can add!

# Here are some methods you can use to edit your CSS with jQuery:
+ addClass() - Adds one or more classes to the selected elements
+ removeClass() - Removes one or more classes from the selected elements
+ toggleClass() - Toggles between adding/removing classes from the selected elements
+ css() - Sets or returns the style attribute

# JavaScript Events
In JavaScript, events are user actions such as mouse clicks, key presses, or window resizing. We can define code that will be run when those events happen.

JavaScript allows us to bind - or connect - functions to particular events. We create a function, and then tell the browser to run that function whenever that event happens.

jQuery lets us bind events with a concise, readable syntax. In the example below, lets pretend we wanted to do something everytime the user clicked on a header.

```js
$("h1").click(action);
```

* `$("h1")` - the *listener* - uses the selector syntax `$()` to get all the `<h1>` elements
* `click` - the *event* we are responding to
* `action` - the *handler* - or what we want our response to be

JavaScript gives us a few different ways to create the 'action', by using a named method or using a callback function.

# Named Methods as Event Handlers

We can define a named method. Then we can pass that method as a parameter when we call the event:

```js
function tellUsWeClicked () {
    alert("You clicked a header");
}

$("h1").click(tellUsWeClicked);
```


# Callback Functions as Event Handlers

We can also use an anonymous function: `function(){}` as the parameter. It's anonymous because we create it without giving it a name. The code for the function will go in between the curly brackets. This is a common pattern, called a callback function.

```js
$("h1").click(function(){
    alert("You clicked a header");
});
```

Especially if that function is not going to be used anywhere else, this style of coding makes it easy to read off exactly what will happen when the click event is triggered.

# Other Event handlers
jQuery can respond to a wide variety of Events which you should read about in the documentation.
#### Some popular ones are:
+ Mouse clicks
+ Page load finishing
+ Moving the mouse over an element (often used for menu highlights)
+ Submitting an HTML form
+ Pressing the keyboard buttons
+ And MORE!!

# Document Ready as an Event
We often only want to run our JavaScript when the page has finished loading. Just like we can bind functions to events triggered by the user, we can run certain functions when the document is ready.

```js
$( document ).ready(function() {
  // Here are all the functions that
  // will be run when the document is ready.
});
```

# $(this) inside Event callbacks
 $(this) allows you to easily access the element that fired the event.
For Example:

```js
$("h1").click(function(){
    alert("You clicked a header");
    $(this).fadeOut();
});
```

Here, the $(this) refers to the header that was just clicked.  After the user click on the header, an alert will pop up and then that header will fade out.

# Chaining Methods
Up until this point we've been writing jQuery statements one at a time. However, there's a convenient way to do multiple things to an element without writing so much code - you can chain multiple commands together.

For example, if we wanted an element to turn blue, and then move up and down we could write it this way:

```js
$(this).css("color", "blue");
$(this).slideUp(2000);
$(this).slideDown(2000);
```

This works, but we're repeating the lookup for the HTML element with the ID of stuff multiple times.

Instead we can do this:

```js
$(this).css("color", "blue").slideUp(2000).slideDown(2000);
```

Here, we've chained the methods by simply adding the next one to the end of the chain.

# Conclusion:
jQuery and other libraries allow you to do amazingly complex stuff with a simple function call. Any developer worth their salt will want to make a website that responds to the user. jQuery events let you do that.

Now it's time to explore events and event handlers! Try some of the jQuery you've been learning to change elements and style when certain actions happen. [Here's a list](http://help.dottoro.com/larrqqck.php) of a ton of browser events that your code can listen for.

Some of the most common are 'click', 'scroll', 'mouseenter' and 'mouseleave', 'focus', 'blur',  and 'keyup'. There are lots and lots of events - what events do popular websites listen for and handle?
