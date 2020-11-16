<div class="border">
<img class="instructor-image" src="../../instructor-avatar/tariqProfile300x300.png"></img>

<div class="title-slide">
    <h1>Lets Code!</h1>
    <h3>OOP: Four Pillars of OOP</h3>
    <p>Instructor: Tariq Hook</p>
    <p>You can find me on github @code-rhino</p>
</div>
</div>

-
-

<h2>Key <span class="black">Terms</span></h2>

<div class="livecode livecode-2p">

<div class="col">

* Four Pillars
	* Encapsulation
	* Inheritance
	* Polymorphism
	* Abstraction

</div>
<div class="col">


</div>
</div>


-
-

 <!-- .element class="info-splash" -->

![image](./imgs/java.png)<!-- .element class="corner-image" -->

<div class="info-splash-content">


## Encapsulation

</div>

-

<div class="slide-with-border">

## Encapsulation
* also known as _data hiding_.
* mechanism of wrapping the data (variables) and code acting on the data (methods) together as a single unit.
* variables of a class are hidden from other classes, and can be accessed only through the methods of their current class.

</div>

-

<div class="slide-with-border">

## Achieving Encapsulation
* Achieved by wrapping several data fields and methods in a single entity

```java
public class Person {
  private String name;
  private Integer age;
  public Person(String name, Integer age) {
    this.name = name;
    this.age = age;
  }
  // getters and setters omitted for brevity
}
```
</div>

-

<div class="slide-with-border">

### Encapsulation<br>Managing person-data<br>without Encapsulation
* Unrelated variables coexist in scope

```java
// setting name and age of leon
String tariqName = "Tariq";
Integer tariqAge = 41;

// setting name and age of wilhem
String froilanName = "Froilan";
Integer froilange = 41;

// changing state of leon
tariqName = "Tariq";
tariqAge = 42;

// changing state of wilhem
froilanName = "Froilan";
froilanAge = 24;
```


-

<div class="slide-with-border">

### Encapsulation<br>Managing person-date<br>with Encapsulation
* Related variables coexist in related scope

```java
public void demo() {
    // setting name and age of leon
    Person tariq = new Person("Tariq", 41);

    // setting name and age of wilhem
    Person froilan = new Person("Froilan", 41);

    // changing name of tariq
    tariq.setName("Tariq");
    tariq.setAge(42);

    // changing name of wilhem
    froilan.setName("Froilan");
    froilan.setAge(42);
}
```



-
-
 <!-- .element class="info-splash" -->

![image](./imgs/java.png)<!-- .element class="corner-image" -->

<div class="info-splash-content">


## Inheritance

</div>

-

<div class="slide-with-border">

## Inheritance
* the process where one class acquires the members (methods and fields) of another.
* Ensures information is made manageable in a hierarchical order.
*  Inheritance is achieved in java by use of the keyword _extends_ or _implements_


</div>

-


<div clas ="slide-with-border">

### Inheritance<br>Designing an Animal class
* the class whose properties are inherited is known as _superclass_ (base-class).
  * Here, the `Animal` class is intended to be the super class.

```java
public class Animal {
  private Point position;
  protected String phrase;

  public Animal(String phrase) { this.phrase = phrase; }

  public void setPosition(Integer xPosition, Integer yPosition) {
    this.position = new Point(xPosition, yPosition);
  }

  public Point getPosition() { return this.position; }
}
```

</div>

-

<div class="slide-with-border">

### Inheritance<br>Designing a Fox class
* The class which inherits the members of other is known as _subclass_ (derived class)
  * Here, the `Fox` class inherits members from `Animal`
  * Notice, `Fox`'s reference to _protected_ member of `phrase`.

```java
public class Fox extends Animal {
  public Fox() {
    super("Bark!");
  }

  public void useSpeech() {
    System.out.println(super.phrase); // inherited member
  }
}
```

</div>

-

<div class="slide-with-border">

### Inheritance<br>Accessing Animal Properties
```java
public void demo() {
  Fox fox = new Fox();
  Point foxPosition = fox.getPosition() // method of `Animal` class
  System.out.println(foxPosition);
}
```

Output
```java
null
```
</div>

-

<div class="slide-with-border">

### Inheritance<br>Accessing Animal Properties
* _protected_ members are only accessible from within the scope of the inheriting _subclass_.
```java
public void demo() {
    Fox fox = new Fox();
    String phrase = fox.phrase; // invalid reference
}
```

-
-
 <!-- .element class="info-splash" -->

![image](./imgs/java.png)<!-- .element class="corner-image" -->

<div class="info-splash-content">


## Polymorphism

</div>

-

<div class="slide-with-border">

## Polymorphism
* ability to take on different forms or stages
* Dynamic (run-time) polymorphism: JVM, rather than compiler, decides which method to call
* Static (compile-time) polymorphism: compiler identifies method to call by method-signature

</div>

-

<div class="slide-with-border">

### Dynamic Polymorphism
* Also known as _run time_ polymorphism
* The Java compiler does not understand which method to call, the decision is deferred to JVM at run-time.
* _Method overriding_ of instance methods is an example of dynamic polymorphism in Java


</div>

-

<div class="slide-with-border">

### Dynamic (Runtime) Polymorphism<br>Designing Bird class
* The following design enforces polymorphic behavior of a `Bird`

```java
public interface Flyer { void fly(int distance); }
```
```java
public abstract class Animal { String speak(); }
```
```java
public class Bird extends Animal implements Flyer {
  @Override
  public void fly(int distance) {
    this.setLocation(getX(), getY()+distance);
  }

  @Override
  public String speak() {
    return "chirp!"
  }
}
```
</div>

-

<div class="slide-with-border">

### Dynamic (Runtime) Polymorphism<br>Bird Example
* `Bird` as `Animal` exposes only `speak` method.

```java
public void demo() {
  Animal animal = new Bird();
  animal.speak();
}
```


-
### Dynamic (Runtime) Polymorphism<br>Bird Example
* `Bird` as `Flyer` exposes only `fly` method.

```java
public void demo() {
  Flyer flyer = new Bird();
  flyer.fly(10);
}
```
</div>

-

<div class="slide-with-border">

### Dynamic (Runtime) Polymorphism<br>Bird Example
* `Bird` as `Bird` exposes `speak` and `fly` method.

```java
public void demo() {
  Bird bird = new Bird();
  bird.speak();
  bird.fly(10);
}
```
</div>

-

<div class="slide-with-border">

### Static Polymorphism
* Also known as _compile-time polymorphism_ or _static binding_
* At compile time, Java knows which method to invoke by checking the method signatures.


</div>

-

<div class="slide-with-border">

### Static (compile-time) Polymorphism<br>Designing Person class
* The following design enforces polymorphic behavior of a `Person` by overloading the constructor

```java
public class Person {
  private String name;
  private Integer age;
  private Color eyeColor;

  public Person(String name, Integer age, Color eyeColor) {
    this.name = name;
    this.age = age;
    this.eyeColor = eyeColor;
  }

  public Person() {
    this("Leroy", 50, Color.BLACK);
  }
}
```

</div>

-

<div class="slide-with-border">

### Static (compile-time) Polymorphism<br>Person Example
* _Primary_ constructor of `Person` class

```java
public void demo() {
  String personName = "Jamar";
  Integer personAge = 25;
  Color personEyeColor = Color.BROWN;
  Person person = new Person(personName, personAge, personEyeColor);

  System.out.println(person.getName());
  System.out.println(person.getAge());
  System.out.println(person.getEyeColor());
}
```

Output
```java
Jamar
25
BROWN
```

</div>

-

<div class="slide-with-border">

### Static (compile-time) Polymorphism<br>Person Example
* _Nullary_ constructor of `Person` class

```java
public void demo() {
  Person person = new Person();

  System.out.println(person.getName());
  System.out.println(person.getAge());
  System.out.println(person.getEyeColor());
}
```

Output
```java
John
50
BLACK
```


-
-

 <!-- .element class="info-splash" -->

![image](./imgs/java.png)<!-- .element class="corner-image" -->

<div class="info-splash-content">


## Abstraction

</div>

-

<div class="slide-with-border">

## Abstraction
* the process of exposing essential features of an entity while hiding other irrelevant detail.
* abstraction reduces code complexity and at the same time it makes your aesthetically pleasant.

</div>

-

<div class="slide-with-border">

### Abstraction
* Fetching & printing user input without abstraction
```java
public void withoutAbstraction() {
    InputStream inputStream = System.in;
    Scanner scanner = new Scanner(inputStream);
    String promptName = "What is your name?";
    String promptAge = "What is your age?";

    System.out.println(promptName);
    String stringName = scanner.nextLine();

    System.out.println(promptAge);
    String stringAge = scanner.nextLine();
    Integer intAge = Integer.parseInt(stringAge);

    System.out.println("Name = " + stringName);
    System.out.println("Age = " + intAge);
}
```


</div>

-

<div class="slide-with-border">

### Abstraction
* Fetching & printing user input with abstraction

```java
public void withAbstraction() {
    IOConsole console = new IOConsole();
    String promptName = "What is your name?";
    String promptAge = "What is your age?";
    String userInputName = console.getStringInput(promptName);
    Integer userInputAge = console.getIntegerInput(promptAge);
    Person person = new Person(userInputName, userInputAge);
    console.print(person.toString());
}
```

-
-

<h2>Wrap <span class="black">Up</span></h2>

<div class="livecode livecode-2p">

<div class="col">

* Four Pillars
	* Encapsulation
	* Inheritance
	* Polymorphism
	* Abstraction

</div>
<div class="col">


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