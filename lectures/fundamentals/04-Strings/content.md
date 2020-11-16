<div class="border">
<img class="instructor-image" src="../../instructor-avatar/tariqProfile300x300.png"></img>

<div class="title-slide">
    <h1>Lets Code!</h1>
    <h3>Fundamentals: Strings</h3>
    <p>Instructor: Tariq Hook</p>
    <p>You can find me on github @code-rhino</p>
</div>
</div>
-
-

<h2>Key <span class="black">Terms</span></h2>

<div class="livecode livecode-2p">

<div class="col">

* Immutable
* Substring
* Concatenation



</div>
<div class="col">

* Equality 

</div>
</div>

-
-

 <!-- .element class="info-splash" -->

![image](./imgs/java.png)<!-- .element class="corner-image" -->

<div class="info-splash-content">


## Strings

</div>
-

<div class="slide-with-border">

## Strings

Java does not have a built-in string type. Instead, the standard Java library contains a predefined class called String.

```
String e = ""; // an empty string
String greeting = "Hello";
```


</div>

-
<div class="slide-with-border">

### Substrings

You can extract a substring from a larger string with the substring method of the String class.

```
String greeting = "Hello";
String s = greeting.substring(0, 3);
```

The second parameter of substring is the first position that you do not want to copy.

</div>

-

<div class="slide-with-border">

### Concatenation

Use + to join (concatenate) two strings.

```
String expletive = "Expletive"; String PG13 = "deleted";
String message = expletive + PG13;
```

</div>

-

<div class="slide-with-border">

When you concatenate a string with a value that is not a string, the latter is converted to a string.

```
int age = 13;
String rating = "PG" + age;
```

```
String all = String.join(" / ", "S", "M", "L", "XL"); // all is the string "S / M / L / XL"
```

</div>

-

<div class="slide-with-border">

### Strings Are Immutable

The String class gives no methods that let you change a character in an existing string.

```
greeting = greeting.substring(0, 3) + "p!";
```

Since you cannot change the individual characters in a Java string, the documentation refers to the objects of the String class as immutable.

</div>

-

<div class="slide-with-border">

### Testing Strings for Equality

To test whether two strings are equal, use the equals method.

```
s.equals(t)

"Hello".equals(greeting)

"Hello".equalsIgnoreCase("hello")
```

Do not use the == operator to test whether two strings are equal

</div>

-
<div class="slide-with-border">

### Empty and Null Strings

The empty string "" is a string of length 0.

`if (str.length() == 0)`

or

`if (str.equals(""))`

</div>

-

<div class="slide-with-border">

However, a String variable can also hold a special value, called null

```
if (str == null)

if (str != null && str.length() != 0)
```
</div>
-
-

 <!-- .element class="info-splash" -->

![image](./imgs/java.png)<!-- .element class="corner-image" -->

<div class="info-splash-content">


### Reading the Online API Documentation

</div>

-

<div class="slide-with-border">

### Building Strings

Using the StringBuilder class allows you to build a string from many small pieces.

```
StringBuilder builder = new StringBuilder();

builder.append(ch); // appends a single character
builder.append(str); // appends a string

String completedString = builder.toString();
```

</div>

-
-
<h2>Wrap <span class="black">Up</span></h2>

<div class="livecode livecode-2p">

<div class="col">

* Immutable
* Substring
* Concatenation



</div>
<div class="col">

* Equality 

</div>
</div>

-
-



 <!-- .element class="info-splash" -->

![image](./imgs/java.png)<!-- .element class="corner-image" -->

<div class="info-splash-content">


## Keep Coding !!!
### Clean Code is Happy Code

</div>