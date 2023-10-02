# Why use node-based data structures
Arrays are quite simple. You declare a structure of a specific size and write elements to it. The memory used to allocate this structure might as well be viewed as a sheet of paper. It's blank at first and can be filled in with things as you go.

In c++ this is quite literal as these arrays are allocated in contiguous memory locations, and all values can be accessed using the original identifier, with the proper index.

>[!info] Arrays in c++
>```cpp
>//dynamically declared array (heap memory)
>int* a = new int[10];
>//statically declared array (static memory)
>int a[10];
>```

The problem with that approach is that you can run out of space or allocate too much space if you don't know how many elements you'll have beforehand.

>[!info] Resizable arrays
>Resizable arrays exist however their implementation suffers from the drawback of their allocation style. 
>Since you can't reliably find new memory around the already allocated array, in order to resize it a bigger array is created and all the elements are copied over from the old array tot the new array. The new array is typically double the size of the old one since that makes for optimal performance. The big O of adding elements to such arrays is typically referred to as "amortized".
> [This](https://youtu.be/algDLvbl1YY?si=Qo8UeVcOWhdPyw4l) video describes this process in a fairly intuitive way.

This is where **node-based** data structures come in. The most basic ones are linked lists. Their internal functionality is fundamentally different to arrays. Their.obsidian/workspace/* elements are not allocated in one go and are not next to each other in memory. Instead each element lives in a **node** structure that gets allocated in heap memory. 

In order to maintain reference to all the values in the structure each node has at least one pointer (or maybe several) that points to a different node. This leaves us with a limited amount of direct references in the encompassing structure and all other references are obtained by going node to node and using the available nodes to obtain references to other ones.

Node-based structures come with a drawback though, since you can't directly access all values like in arrays, sometimes you have to spend time going though the structure to find the needed element.

## Linked lists
A linked list consists of a series of nodes, where each node holds a data element and a reference (or pointer) to the next node in the sequence. Linked lists come in various forms, but the most common type is the singly linked list:

![[LinkedList.excalidraw.svg|700]]

Singly-linked list structures can be used to implement structures like **queues** and **stacks**.

 >[!note] Priority Queues and Stacks
 >Priority queues and stacks are special types of queues and stacks that accept a priority index along with an element value. When popping an element from such structure the value with a minimum/maximum priority index will be returned.
 >These can also be implemented via node-based structures.
### Queues 
A queue is a linear data structure that follows the **First-In-First-Out (FIFO) principle**. It means that the element that enters the queue first will be the first to be removed.

A **node-based queue** implementation can be found below:
#### General structure
![[Queue.excalidraw.svg|700]]
#### Element addition
![[QueueAdd.excalidraw.svg|700]]
#### Element removal
![[QueueRemove.excalidraw.svg|700]]

### Stacks
A stack is a linear data structure that follows the **Last-In-First-Out (LIFO) principle**. This means that the last element added to the stack will be the first one to be removed.

A **node-based stack** implementation can be found below:
#### General Structure 
![[Stack.excalidraw.svg|600]]
#### Element addition
![[StackAdd.excalidraw.svg|600]]
#### Element removal
![[StackRemove.excalidraw.svg|600]]

