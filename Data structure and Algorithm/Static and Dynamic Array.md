# Static and Dynamic Array

## What is Static array
Static Array is a fixed size container for data which indexes is started from zero.<br/>

It is also indexable which mean each slot in a static array can be referenced by a index.<br/>

Usually, static array are stored continously inside memory so we can access all element by knowing the inital address and offset.<br/>

<i> P.S. There is also stack heap structure in some programming languages which will store any static data type in the stack and its size must be known at compile time.</i>

## When and Where do we use Static Array
Static Array is used anywhere.For example,<br/>
We can use it to store collection of data , storing objects , act as a buffer for reading large file , using in dynamic programming<br/>

There is no a particular use case because it is widely use in lots of situation

## Complexity of Static Array and Dynamic Array
To know the complexity of Static Array and Dynamic Array,we need to know the operation we can act on them.

<table>
    <tr>
        <td>Operation</td>
        <td>Static Array</td>
        <td>Dynamic Array</td>
    </tr>
    <tr>
        <td>Access</td>
        <td>O(1)</td>
        <td>O(1)</td>
    </tr>
    <tr>
        <td>Standard Search</td>
        <td>O(n)</td>
        <td>O(n)</td>
    </tr>
    <tr>
        <td>Insertion</td>
        <td>Not supported</td>
        <td>O(n)</td>
    </tr>
    <tr>
        <td>Deletion</td>
        <td>Not supported</td>
        <td>O(n)</td>
    </tr>
    <tr>
        <td>Appending</td>
        <td>Not supported</td>
        <td>O(1)</td>
    </tr>
</table>

## What is a dynamic array and some operations example
Dynamic Array is a data structure that can change size during run-time , it support insertion and deletion.<br/>
It inherited the advantage of random access using index from static array but it can change size through out the program

## What is the advantage of dynamic array and static array
For dynamic array, it provide better flexibility especially when we don't know the size of the input.However, it may also cause memory leak and bug in the program.<br/>

<i>P.S. Usually, more flexibility equal to more error prone</i><br/>

For Static array, it is less error prone and cleaner implementation for fixed input, also the compiler can optimized the machine code of a static array which result in faster access (Minimal but still note worthy).However, it lack flexibility as it can't change size at any given time.
## Implementation of Dynamic Array
There are lots of way to implement dynamic array.In most modern programming language, it usually already provide some sort of dynamic array for us.<br/>

To implement a dynamic array, We can use a static array to store the inital array.Upon deletion or insertion(when it is full), we can create a new array and copy the contents of the inital array over. We can also use pointer or even double pointer to implement a dynamic array.

## Part of Source code of building Dynamic Array using static array
We will only look at some interesting part espcially on deletion and insertion.

Note that T is generic type for Java
```java
public void add(T elem) {

    // Time to resize!
    if (len + 1 >= capacity) {
      if (capacity == 0) capacity = 1;
      else capacity *= 2; // double the size
      T[] new_arr = (T[]) new Object[capacity];
      for (int i = 0; i < len; i++) new_arr[i] = arr[i];
      arr = new_arr; // arr has extra nulls padded
    }

    arr[len++] = elem;
  }

  // Removes an element at the specified index in this array.
  public T removeAt(int rm_index) {
    if (rm_index >= len || rm_index < 0) throw new IndexOutOfBoundsExceptio();
    T data = arr[rm_index];
    T[] new_arr = (T[]) new Object[len - 1];
    for (int i = 0, j = 0; i < len; i++, j++)
      if (i == rm_index) j--; // Skip over rm_index by fixing j temporarily
      else new_arr[j] = arr[i];
    arr = new_arr;
    capacity = --len;
    return data;
  }

  public boolean remove(Object obj) {
    int index = indexOf(obj);
    if (index == -1) return false;
    removeAt(index);
    return true;
  }

  public int indexOf(Object obj) {
    for (int i = 0; i < len; i++) {
      if (obj == null) {
        if (arr[i] == null) return i;
      } else {
        if (obj.equals(arr[i])) return i;
      }
    }
    return -1;
  }
```