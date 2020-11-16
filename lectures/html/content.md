<div class="border">
<img class="instructor-image" src="../instructor-avatar/val-fragier.png"></img>

<div class="title-slide">
    <h1>Lets Code!</h1>
    <h2>Intro to HTML</h2>
    <p>Instructor: Val Fragier</p>
    <p>You can find me on github @valfragier16</p>
</div>
</div>

-
-

<div class="slide-with-border">

## Intro to HTML, and CSS
### Part 1: HTML

</div>

-
-

<div class="slide-with-border">

## What is HTML?

* Stands for Hyper Text Markup Language
* A markup language
    * defines the **structure** and **semantics** of webpage content through a series of elements.
* **Not** a programming language

</div>
-
<div class="slide-with-border">

## What is an HTML Element?

<img src="img/html-element.png" />

* Tag Name/Type
* Opening Tag
* Closing Tag
* Content

</div>
-
<div class="slide-with-border">

## What is an HTML Attribute

<img src="img/html-attribute.png" />

Here, `class` is the attribute name and `editor-note` is the value

An attribute should always have:
* A space between it and the element name (or the previous attribute, if the has more than one attribute).
* The attribute name, followed by an equals sign.
* Opening and closing quote marks wrapped around the attribute value.  

</div>
-
<div class="slide-with-border">

## Nesting elements

You can place HTML elements inside other elements, but mind your opening and closing tags.

Correct
```html
<p>My cat is <strong>very</strong> grumpy.</p>
```

Incorrect
```html
<p>My cat is <strong>very grumpy.</p></strong>
```

</div>
-
<div class="slide-with-border">

## Empty Elements

Some elements do not have content, so they are self closing. Take `img` as an example: it has two attributes `src` and `alt`, but no content.

```html
<img src="images/cd-logo.png" alt="Code Differently">
```

</div>
-
<div class="slide-with-border">

## Anatomy of an HTML Document

HTML elements aren't very useful on their own. We combine them to form an entire HTML page.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My test page</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="My test image">
  </body>
</html>
```

</div>
-
<div class="slide-with-border">

## Anatomy of an HTML document

* ``<!DOCTYPE html>`` - Tells the browsers to interpret this document as an HTML document
* ``<html></html>`` — Wraps all the content on the entire page, and is sometimes known as the root element.
* ``<head></head>`` — Acts as a container for all the stuff you want to include on the HTML page that isn't the content you are showing to your page's viewers. This can include [metadata](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML) like keywords or a description you want to show to search engines, CSS to style your page, and more.

</div>
-
<div class="slide-with-border">

## Anatomy of an HTML document

* ``<meta charset="utf-8">`` — this element sets the character set your document should use to UTF-8, which includes most characters from the vast majority of human written languages.
* ``<title></title>`` — Sets the title of your page, which is the title that appears in the browser tab the page is loaded in. It is also used to describe the page when you bookmark/favourite it.
* ``<body></body>`` — Contains all the content that you want to show to web users when they visit your page, whether that's text, images, videos, buttons or whatever else.

</div>

-
-

<div class="slide-with-border">


## Block vs Inline Element

HTML elements are categorized as either block-level or inline-level elements. 

A block-level element occupies the entire space of its parent element (container).

Inline elements are those which only occupy the space bounded by the tags defining the element, instead of breaking the flow of the content. 

</div>
-
<div class="slide-with-border">

## Block Level Elements

<img src="img/block.png" />

-

## Inline Level Elements

<img src="img/inline.png" />

</div>
-
-
<div class="slide-with-border">

## Basic HTML Elements

</div>
-
<div class="slide-with-border">

## Headings - Block Level

Heading elements allow you to specify that certain parts of your content are headings — or subheadings — of your content. 

HTML allows for 6 levels of heading, though you'll typically only use 1 - 4.

```html
<h1>My main title</h1>
<h2>My top level heading</h2>
<h3>My subheading</h3>
<h4>My sub-subheading</h4>
```

</div>
-
<div class="slide-with-border">

## Paragraphs - Block Level

``<p>`` elements are for containing paragraphs of text; you'll use these frequently when marking up regular text content:

```html
<p>This is a single paragraph</p>
```
</div>
-
<div class="slide-with-border">

## Lists - Block Level

Marking up lists always consist of at least two elements, either `ul` or `ol` and `li`. The most common list types are ordered and unordered lists:

* Unordered lists are for lists where the order of the items doesn't matter, like a shopping list. These are wrapped in a ``<ul>`` element.
* Ordered lists are for lists where the order of the items does matter, like a recipe. These are wrapped in an ``<ol>`` element.

</div>
-
<div class="slide-with-border">

## Lists - Block Level

```html
<p>Code Differently is a community of dedicated</p>
<ul>
    <li>Staff</li>
    <li>Instructors</li>
    <li>Students</li>
</ul>

<p>To apply to Code Differently:</p>
<ol>
    <li>Submit an application</li>
    <li>Attend a group interview</li>
    <li>Take our assessment test</li>
</ol>
```

</div>
-
<div class="slide-with-border">

## Images - Inline

Embed an image onto the page with the `<img/>` tag.

```html
<img src="images/cd-logo.png" alt="Code Differently" title="Code Differently" />
```

* ``src`` - path to the location of the image file
* ``alt`` - description of the photo intended for when the file cannot be found, or for use by users with visual impairments
* ``title`` - description of the photo that will appear as a tooltip when the image is hovered over

</div>
-
<div class="slide-with-border">

## Links - Inline

To add a link, use the ``<a></a>`` tag, "a" being short for "anchor". You can use absolute or relative uri paths. Content of the a tag can be text or another html element like an image.

```html
<a href="https://www.codedifferently.com">Code Differently</a>

<a href="/apply">Apply Now</a>

<a href="https://www.codedifferently.com">
    <img src="images/cd-logo.png" alt="Code Differently" title="Code Differently" />
</a>
```

``href`` - short for hyperlink reference. Designates the uri you'd like to link to.

</div>
-
<div class="slide-with-border">

## Forms - Block

Forms consist of many individual html elements. All HTML forms start with a <form> element, which can contain various form controls.

```html
<form>
    <label for="firstName"></label>
    <input id="firstName" type="text" />
</form>
```

</div>
-
<div class="slide-with-border">

## Input - Block

The most common type of form control is ``<input>``. Input is a self closing element that can have various types, including:

* [Text](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/text) - ``<input type="text"/>``
* [Checkbox](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/checkbox) - ``<input type="checkbox"/>``
* [Radio](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/radio) - ``<input type="radio"/>``
* [Password](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/password) - ``<input type="password"/>``
* [Email](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/email) - ``<input type="email"/>``
* [Button](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/button) - ``<input type="button"/>`` could also substitute ``<button>``
* [Submit](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/submit) -  ``<input type="submit"/>``

</div>
-
<div class="slide-with-border">

## Semantic Container Elements

In addition to defining individual parts of your page (such as "a paragraph" or "an image"), HTML also has a number of **semantic** elements used to define areas of your website, like the header, navigation menu, or main content. 

</div>
-
<div class="slide-with-border">

## Basic Sections of an HTML Document

* ``header`` - ``<header>`` Block level. Typically a big strip across the top with a big heading and/or logo.
* ``navigation bar`` - ``<nav>`` Block level. Typically links to the site's main sections; usually represented by menu buttons, links, or tabs.
* ``main content`` - ``<main>`` Block level. Typically a big area in the center that contains most of the unique content of a given webpage.

</div>
-
<div class="slide-with-border">

## Basic Sections of an HTML Document

* ``sidebar`` - ``<sidebar`` Block level. Typically some supporting info, links, quotes, ads, etc.
* ``footer`` - ``<footer>`` Block level. A strip across the bottom of the page that generally contains fine print, copyright notices, or contact info.
-

## Basic Sections of an HTML Document

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">

    <title>My page title</title>
    <link href="https://fonts.googleapis.com/css?family=Open+Sans+Condensed:300|Sonsie+One" rel="stylesheet" type="text/css">
    <link rel="stylesheet" href="style.css">
    <!-- the below three lines are a fix to get HTML5 semantic elements working in old versions of Internet Explorer-->
    <!--[if lt IE 9]>
      <script src="https://cdnjs.cloudflare.com/ajax/libs/html5shiv/3.7.3/html5shiv.js"></script>
    <![endif]-->
  </head>

  <body>
    <!-- Here is our main header that is used across all the pages of our website -->
    <header>
      <h1>Header</h1>
    </header>

    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Our team</a></li>
        <li><a href="#">Projects</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>

    <!-- Here is our page's main content -->
    <main>
      <!-- It contains an article -->
      <h2>Article heading</h2>

      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Donec a diam lectus. Set sit amet ipsum mauris. Maecenas congue ligula as quam viverra nec consectetur ant hendrerit. Donec et mollis dolor. Praesent et diam eget libero egestas mattis sit amet vitae augue. Nam tincidunt congue enim, ut porta lorem lacinia consectetur.</p>

      <h3>subsection</h3>

      <p>Donec ut librero sed accu vehicula ultricies a non tortor. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aenean ut gravida lorem. Ut turpis felis, pulvinar a semper sed, adipiscing id dolor.</p>

      <h3>Another subsection</h3>

      <p>Donec viverra mi quis quam pulvinar at malesuada arcu rhoncus. Cum soclis natoque penatibus et manis dis parturient montes, nascetur ridiculus mus. In rutrum accumsan ultricies. Mauris vitae nisi at sem facilisis semper ac in est.</p>

      <!-- the aside content can also be nested within the main content -->
      <aside>
        <h2>Related</h2>
    
        <ul>
          <li><a href="#">Oh I do like to be beside the seaside</a></li>
          <li><a href="#">Oh I do like to be beside the sea</a></li>
          <li><a href="#">Although in the North of England</a></li>
          <li><a href="#">It never stops raining</a></li>
          <li><a href="#">Oh well...</a></li>
        </ul>
      </aside>
    </main>

    <!-- And here is our main footer that is used across all the pages of our website -->
    <footer>
      <p>©Copyright 2050 by nobody. All rights reversed.</p>
    </footer>
  </body>
</html>
```

</div>
-
<div class="slide-with-border">

## Generic Container Elements

When you want to group content that doesn't fit one of the semantic html elements, you can use ``div``, a block level element, or ``span``, an inline element.

These are especially useful when you want to target a group of elements with CSS or JS.

</div>
-
<div class="slide-with-border">

## Span

``<span>`` is an inline non-semantic element, which you should only use if you can't think of a better semantic text element to wrap your content, or don't want to add any specific meaning.

```html
<p>The King walked drunkenly back to his room at 01:00, the beer doing nothing to aid
him as he staggered through the door <span class="editor-note">[Editor's note: At this point in the
play, the lights should be down low]</span>.</p>
```

</div>
-
<div class="slide-with-border">

## Div

``<div>`` is a block level non-semantic element, which you should only use if you can't think of a better semantic block element to use, or don't want to add any specific meaning.

```html
<div class="shopping-cart">
  <h2>Shopping cart</h2>
  <ul>
    <li>
      <p><a href=""><strong>Cashmere sweater</strong></a>: $99.95.</p>
      <img src="../products/3333-0985/thumb.png" alt="Cashmere sweater">
    </li>
    <li>
      ...
    </li>
  </ul>
  <p>Total cost: $237.89</p>
</div>
```

</div>
-
-

<div class="slide-with-border">

## Intro to HTML, and CSS
### Part 2: CSS

</div>
-
<div class="slide-with-border">

## What is CSS?

CSS stands for Cascading Style Sheets. It is a style sheet language for expressing the presentation, including colors, layout, sizes, and more, of a structured document like HTML, XML or SVG.
CSS applies styles through CSS rules.

</div>
-
<div class="slide-with-border">


## What is a CSS rule?

* ``selector`` - selects the element(s) you want to apply the updated property values to. 
* ``properties`` - A set of properties with corresponding values set to update how the HTML content is displayed.

```CSS
header {
    background-color: teal;
    height: 160px;
}
```
</div>
-
<div class="slide-with-border">

## Using HTML and CSS

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My CSS experiment</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>This is my first CSS example</p>
  </body>
</html>
```

```CSS
h1 {
  color: pink;
  background-color: aqua;
  border: 1px solid purple;
}

p {
  color: green;
}
```

</div>
-
<div class="slide-with-border">

## How does CSS work?

When a browser displays a document, it must combine the document's content with its style information. It processes the document in two stages:

* Converts HTML and CSS into the DOM (Document Object Model)
    * The DOM represents the document in the computer's memory, combining the document's content with its style.
* Displays the contents of the DOM

</div>
-
<div class="slide-with-border">

## What is the DOM

The Document Object Model (DOM) is a **programming interface** for HTML and XML documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects. That way, programming languages can connect to the page.

</div>
-
<div class="slide-with-border">

## The DOM Tree

The DOM has a tree-like structure. Each element, attribute and piece of text in HTML becomes a DOM node. Nodes are defined by their relationship to other nodes. Some elements are parents of child nodes, and child nodes have siblings.

```html
<p>
  Welcome to:
  <span>Code</span>
  <span>Differently</span>
</p>
```

```
P
├─ "Welcome to:"
├─ SPAN
|  └─ "Code"
├─ SPAN
  └─ "Differently"

```

-

## How does CSS work?

<img src="img/how-css-works.png" />

</div>
-
<div class="slide-with-border">

## Applying CSS to the DOM

```CSS
span {
  background-color: aqua;
}
```

<img src="img/CSS-DOM.png" />

</div>
-
<div class="slide-with-border">

## Applying CSS to the DOM

There are 3 ways to apply CSS to an HTML document
* External Stylesheets
* Internal Stylesheets
* Inline Styles

</div>
-
<div class="slide-with-border">
    
## External Stylesheets

Styled through an external stylesheet, linked through the ``<link>`` tag.

index.html
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My CSS experiment</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>This is my first CSS example</p>
  </body>
</html>
```

</div>
-
<div class="slide-with-border">

## External Stylesheets

Styled through an external stylesheet.

style.css
```CSS
h1 {
  color: pink;
  background-color: aqua;
  border: 1px solid purple;
}

p {
  color: green;
}
```
</div>
-
<div class="slide-with-border">

## Internal Stylesheets

Styled through an internal ``<style>`` tag.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My CSS experiment</title>
    <style>
      h1 {
        color: pink;
        background-color: aqua;
        border: 1px solid purple;
      }
      
      p {
        color: green;
      }
    </style>
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>This is my first CSS example</p>
  </body>
</html>
```

</div>
-
<div class="slide-with-border">

## Inline Styles

Styled through the ``style`` property on an individual html element.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My CSS experiment</title>
  </head>
  <body>
    <h1 style="color: pink;background-color: aqua;border: 1px solid purple;">Hello World!</h1>
    <p style="color: green;">This is my first CSS example</p>
  </body>
</html>
```

</div>
-
<div class="slide-with-border">

## CSS Declarations

CSS declarations consist of two building blocks:

* Properties: Human-readable identifiers that indicate which stylistic features (e.g. font, width, background color) you want to change.
* Values: Each specified property is given a value, which indicates how you want to change that property.

</div>
-
<div class="slide-with-border">

## CSS Declarations

A property paired with a value is called a ``CSS declaration``. 

<img src="img/css-syntax.png" />

</div>
-
<div class="slide-with-border">

## CSS Rule Sets

CSS Rule Sets consists of: 
* A CSS Declaration Block
    * One or more CSS declarations
* One or more CSS selectors

<img style="width: 560px" src="img/css-ruleset.png" />

</div>
-
<div class="slide-with-border">

## CSS selectors

CSS selectors are used to target the HTML elements we want to style. There are a wide variety of CSS selectors available, allowing for precise targeting when selecting elements to style. 

</div>
-
<div class="slide-with-border">

## Tag Selectors

You can select elements by their html tag name.

```CSS
/* Targets the < h1 > element */
h1 {
    color: pink;
    font-size: 22px;
}

/* Targets the < header > element */
header {
    height: 160px;
    background-color: blue;
}
```

</div>
-
<div class="slide-with-border">

## Multi Selectors

Applies a single CSS rule set to multiple selectors. Each selector is separated by a comma.

```CSS
h1,
h2,
h3,
h4 {
    color: pink;
    font-size: 22px;
}
```

</div>
-
<div class="slide-with-border">

## Combination selectors

CSS has several ways to select elements based on how they are related to one another. Those relationships are expressed with combinators.

```CSS
/* Specifically targets any < h1 > that 
is a descendant (or nested within)
a < header > */
header h1 {
    color: red;
}

h1 {
    font-size: 32px;
}
```

[All about combining CSS selectors](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Combinators_and_multiple_selectors)

</div>
-
<div class="slide-with-border">

## Evaluating CSS

CSS is read from top to bottom, with declarations later in the file overriding declarations earlier in the file.

```CSS
h1 {
    color: pink;
    font-size: 32px;
    color: blue;
}

h1 {
    color: black;
}
```
``<h1>`` elements will receive a color of black and a font-size of 32px.

</div>
-
<div class="slide-with-border">

## CSS Specificity

CSS rules are also evaluated based on their specificity. If more than one CSS rule sets applies to a particular element, 
and individual CSS declarations are in conflict with one another, the declaration present in the more **specific** CSS ruleset will win.

[All About CSS Specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity)

</div>
-
<div class="slide-with-border">

## CSS Specificity
```html
<body>
    <header>
        <p>I'm an paragraph in the header</p>
    </header>
    <p>
        I'm a p outside of the header
    </p>
</body>
```

```CSS
p {
    color: purple;
    font-size: 16px;
}

header p {
    font-size: 22px;
}
```

<img style="width: 420px" src="img/css-specificity.png" />

</div>
-
<div class="slide-with-border">

## Class selectors

The class selector consists of a dot, `.`, followed by a class name. A class name is any value, without spaces, placed within an HTML class attribute. It is up to you to choose a name for the class. Multiple elements can have the same class value, and a single element can have multiple classes separated by a space.

</div>
-
<div class="slide-with-border">

## Class selectors

```html
<h3>Shopping List</h3>
<ul>
  <li class="priority">Eggs</li>
  <li class="purchased">Butter</li>
  <li class="priority purchased">Milk</li>
</ul>
```

```CSS
.priority {
    font-weight: bold;
}

.purchased {
    text-decoration: line-through;
}
```

<img src="img/css-classes.png" />

</div>
-
<div class="slide-with-border">

## Id Selectors

The ID selector consists of a hash/pound symbol ``#``, followed by the ID name of a given element. Any element can have a **UNIQUE** ID set with the ``id`` attribute. It is up to you to choose an ID name. It's the most efficient way to select a single element.

[Example](https://codepen.io/dominiqueclarke/pen/yRJmPG) 

</div>
-
<div class="slide-with-border">

## The Box Model

<img style="width: 620px" src="img/the-box-model.png" />

</div>
-
<div class="slide-with-border">

## CSS Positioning

[Learn All About CSS Positioning](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout)

-
-

 <!-- .element class="info-splash" -->

![image](./imgs/java.png)<!-- .element class="corner-image" -->

<div class="info-splash-content">


## Keep Coding !!!
### Clean Code is Happy Code

</div>