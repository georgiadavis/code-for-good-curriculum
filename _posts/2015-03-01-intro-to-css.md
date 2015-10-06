---
title: Introduction to CSS
---

# What You Need to Know:
+ HTML Basics

#  What you will Learn:
+	Explain the purpose of CSS
+ How to link to a CSS stylesheet
+	Use CSS selectors to adjust properties of text and images
+	How to use colors in CSS
+ How to use Google Fonts
+ Import Google fonts

# Why This is Important:

So far, all we’ve been able to do is put content on a page with HTML to make some ugly looking websites. So how do we actually make our sites stuff look good?
CSS! CSS stands for Cascading Style Sheets. We write CSS in separate files, so that each file of our web site does one job and one job only.


# Linking our Stylesheet
We write our CSS in a separate file. Each html page must include a reference to the external style sheet file. Notice between the `<head> </head>` tags there is a link that looks like this:

{% highlight html %}
<link rel="stylesheet" type="text/css" href="style.css">
{% endhighlight %}

This links our new playlist_style.css page to our html page so we can apply styling to our HTML file.

# Selectors
Open style.css, let's make our `<h1>` tags a different color. The **selector** defines (or “selects”) which elements these styles apply to.
To make all `<h1>` tags the color red we use a h1 type selector:

{% highlight html %}
h1 {
 color: blue;
}
{% endhighlight %}

The **property-value pairs** in between the curly braces {} are the styles (color: blue sets the text color to blue).
<img src = "https://raw.githubusercontent.com/learn-co-curriculum/cssi-1.5-css-basics/master/images/2.png">
Colons and semicolons are important - they end our statements.


# Various Selectors
There are three kinds of selectors:

+ **Type selector**: selects elements by html tag.
+ **Class selector**: selects all the html tags with the same class attributes.
+ **ID selector**: selects the single html tag by the unique ID attribute. No two HTML elements should have the same id.

<img src= "https://raw.githubusercontent.com/learn-co-curriculum/cssi-1.5-css-basics/master/images/3.png">

Adding a CSS file We’ll define the CSS styles in a separate file. Open playlist_style.css in Atom try changing the colors of the h2 headings.

{% highlight html %}
h2 {
 color: green;
}
{% endhighlight %}

#  Colors
RGB vs Hexadecimal color
There are a few ways to get more specific with color value other than just writing "red".

***RGB***- stands for Red, Green, Blue. The RGB color model is the ways of getting different colors through adding different amounts of Red, Green, and Blue. rgb(0,0,0) gives you black rgb(255,255,255) gives you white

***Hexademical***- is a different notation for the amount of Red, Green, and Blue that gets added to your color.  ``# 000000`` is black ``# ffffff`` is white ``# 0000FF`` is blue (zero amounts of red and green)

The ***Digital Color Meter*** tool on macs is a great resource to find exact color tones.

# Google fonts
Browsers can only display whatever fonts are downloaded on that computer.
If a web application is using some random font that my computer doesn't have, I won't be able to see it.
[Google fonts](https://www.google.com/fonts) is a great resource:

Click the quick view button
<img src="https://raw.githubusercontent.com/learn-co-curriculum/cssi-1.5-css-basics/master/images/6.png">

Scroll down the page till you see this and make sure import is selected:
Copy that the @import url and paste it at the top of your CSS file
<img src="https://raw.githubusercontent.com/learn-co-curriculum/cssi-1.5-css-basics/master/images/7.png">

Integrate the fonts into your CSS:
<img src="https://raw.githubusercontent.com/learn-co-curriculum/cssi-1.5-css-basics/master/images/8.png">

# Conclusion
Now you know how to add styling to your HTML pages. Use different types of selectors to change elements within your HTML page.
