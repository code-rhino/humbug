# Collections: Lists, ArrayLists, LinkedList

-
-

## What we'll cover

<p class="fragment fade-up">What is a List?</p>
<p class="fragment fade-up">The List Interface</p>
<p class="fragment fade-up">ArrayList</p>
<p class="fragment fade-up">LinkedList</p>

-
-

## What is a `Collection`?

* `Collection` is an interface which ensures a class has the ability to hold a series of objects.
* `List` is an interface which _extends_ `Collection`.

-

## Collection Interface

* Fundamental interface for `Collection` classes in java.

```java
public interface Collection<E> extends Iterable<E> {
    boolean add(E element);
    boolean addAll(Collection<? extends E> collection);
    void clear();
    boolean contains(Object object);
    boolean containsAll(Collection<?> collection);
    void foreach(Consumer<E> consumer);
    boolean isEmpty();
    Iterator<E> iterator();
    boolean remove(Object object);
    boolean removeAll(Collection<?> collection);
    boolean retainAll(Collection<?> collection);
    int size();
    Object[] toArray();
    <T> T[] toArray(T[] array);
}
```

-
-

## What is a `List`?

* An ordered collection of elements.
* Users of `List` objects can:
  * access elements by their integer index (position in `List`)
  * insert elements into `List`
  * remove elements from the `List`
  * search for the presence of element in the `List`

-

## List Interface

```java
public interface List<E> extends Collection<E> {
  int lastIndexOf(Object object);
  int indexOf(Object object);
  E set(int index, E object);
  List<E> sub(int startingIndex, int endingIndex);
}
```

-
-

## ArrayList

* `java.util.ArrayList`
* Dynamic in capacity (size)
  * size increases upon insertion, decreases upon removal
* Quicker than `LinkedList` with random access to elements.
* Can only handle _non-primitive_ types.

-

## Unmodifiable List

* `java.util.Arrays.ArrayList`
  * An unmodifiable list, with a stupid name.
  * Should have been named `UnmodifiableList`.

```java
public void demo() {
  String[] array = {"The", "Quick", "Brown", "Fox"};
  List<String> unmodifiableList = Arrays.asList(array);
  unmodifiableList.add("Jumps"); // throws Exception
}
```

Output

```
java.lang.UnsupportedOperationException
```

-

## Converting Array to ArrayList

* populates `ArrayList` upon construction
```java
public void demo() {
  String[] array = {"The", "Quick", "Brown", "Fox"};
  List<String> unmodifiableList = Arrays.asList(array);
  List<String> arrayList = new ArrayList<>(unmodifiableList);
  System.out.println(arrayList);
}
```

Output

```
[The, Quick, Brown, Fox]
```

-

* populates `ArrayList` with `for` each loop (behavior of `Iterable`)

```java
public void demo() {
  String[] phrase = {"The", "Quick", "Brown", "Fox"};
  List<String> list = new ArrayList<>();
  for(String word : phrase) {
    list.add(word);
  }
}
```

-

* populates `ArrayList` with inherited method `Collection.foreach`

```java
public void demo() {
  String[] phrase = {"The", "Quick", "Brown", "Fox"};
  List<String> list = new ArrayList<>(Arrays.asList(phrase));
  list.forEach(word -> list.add(word));
}
```

-
-

## LinkedList

* `LinkedList` is quicker than `ArrayList` at removal/insertion of elements in the middle of the list.
* `LinkedList` values are stored as `Node` objects.
	* Each `Node` is a separate object with a `data` and `next` field.

-

### Node

```Java
class Node<DataType> {
	DataType data;
	Node next;

	Node(DataType d) {
		data = d;
		next = null;
	}
}
```

-

### LinkedList

```java
class LinkedList<DataType> {
  Node<DataType> head;
}
```

-

### LinkedList
* Iterating a linked list
* Requires client to continually check if `next` is null, if not `this.head = next`
