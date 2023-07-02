# Introduction
## What is Data Structure
Data Structure is a way to organize data so that it can be used efficiently
## Why we use Data Structure
We use Data Structure to organize and store Data. <br/>
Data Structure also help us solve problem efficiently (Both time and space)<br/>
Data Structure also made code cleaner and easier to read
## What is the difference between abstract data type (ADT) and data structure
Abstract data type (ADT) is just an abstraction of data structure , it have some rules (operation , structure) that data structure must follow.<br/>

Long strory short, it is just a model/interface that data structure need to follow

However, it won't contain any implementation details.

<table>
    <tr>
        <td>ADT</td>
        <td>Data Structure</td>
    </tr>
    <tr>
        <td>List</td>
        <td>Dynamic Array , Linked List</td>
    </tr>
    <tr>
        <td>Queue</td>
        <td>Linked list queue , stack based queue</td>
    </tr>
    <tr>
        <td>Map</td>
        <td>Hashed Table , Tree map</td>
    </tr>
    <tr>
        <td>Tree</td>
        <td>Binary Tree , avi tree</td>
    </tr>
</table>

## How do we measure the complexity of Algorithm
When we want to measure the complexity of an particular Algorithm, we need to consider two main area which are time and space. <br/><br/>If we need a lots of time to perform a certain task , it will not consider to be efficient. The same case can be applied to space as well
## What and Why is Big O Notation
Big O Notation show us the complexity of an algorithm in worst case scenario. There are also Big theta and Big omega.<br/>

We use big O Notation to measure the complexity of algorithm because generally it is more useful to consider the worst case instead of the best case.<br/><br/>
Big O Notation also help us compare different algorithms as a metric
## What is some properties of Big O notations
When we consider Big O Notation , we usually won't consider the constant and less significant term like 
```
f(n) = 3 + 2n + 3n^2 + 5n^4 / 4 
O(f(n)) = n^4
```

It is because when we Consider input size as infinite , most constant term and less signifant term will not affect as much as the most significant term.<br/>

However,constant term may also affect the complexity of the algorithm in real life (Just we won't consider it when we use Big O Notation)
## Some Big O Notation Example
<table>
     <tr>
        <td>Name</td>
        <td>symbol</td>
        <td>Example</td>
    </tr>
    <tr>
        <td>Constant time</td>
        <td>O(1)</td>
        <td>Loop with fixed time of iteration</td>
    </tr>
    <tr>
        <td>Linear time</td>
        <td>O(n)</td>
        <td>Loop through entire input</td>
    </tr>
    <tr>
        <td>Logarithm time</td>
        <td>O(log(n))</td>
        <td>Binary Search</td>
    </tr>
    <tr>
        <td>Sqaure time</td>
        <td>O(n^2)</td>
        <td>Loop inside Loop with respect to input size</td>
    </tr>
    <tr>
        <td>Factorial time</td>
        <td>O(n!)</td>
        <td>Permutation</td>
    </tr>
</table>