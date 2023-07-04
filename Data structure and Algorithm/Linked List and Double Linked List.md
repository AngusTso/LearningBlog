# Linked List and Double Linked List

## What is a linked list ?
a linked list is a list of nodes that hold data and a reference to the next node.<br/><br/>
A node contain a data part and a reference part (usually a pointer)
<br/><br/>
Usually linked list store node in random place in the memory instead of contigeous address

## Where do we use linked list ?
We can use linked list to construct different data structure like Stack , Queues , List <br/><br/>
We can also model real life object like train<br/><br/>
Widely use to solve Hash Table's hash collision problems<br/><br/>
Implementation of graph adj list implementation.

## Terminology of linked list
<ol>
    <li>Head : The first node of a linked list</li>
    <li>Tail : The last node of a linked list</li>
    <li>Pointer : The reference to next node</li>
    <li>Node : A object consist of data and pointer</li>
</ol>

## Signly Linked list vs Doubly linked list
The major difference between a singly linked list and doubly linked list is that doubly linked list consist of the prev node reference and also the next node reference instead of only referencing the next node.<br/><br/>
This difference yeild a very different performance in various operation and memory usage<br/>
<Table>
    <tr>
        <td></td>
        <td>Pros</td>
        <td>Cons</td>
    </tr>
    <tr>
        <td>Singly linked list</td>
        <td>Less memory usage<br/>simpler implementation</td>
        <td>Can't reference prev node</td>
    </tr>
    <tr>
        <td>Doubly linked list</td>
        <td>Can reference previous and next node</td>
        <td>2x memory usage</td>
    </tr>
</Table>

## Implementation Detail
### Insert Element
### Remove Element

## Complexity analysis

## Code implementation of Doubly Linked list

