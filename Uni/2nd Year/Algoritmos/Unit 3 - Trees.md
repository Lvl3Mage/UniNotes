## Implementing a dictionary
#todo explain what a dictionary is

|  Action  | Vector       |     <     | List          |     <     | Binary Tree  | AVL Tree |
|:--------:|:------------:|:---------:|:-------------:|:---------:|:------------:|:--------:|
|          |  Not sorted  |  Sorted   |  Not sorted   |  Sorted   |              |          |
|  Insert  |      1       |     n     | 1             | n         | n            | log n    |
|  Search  |      n       | log n     | n             | n         | n            | log n    |
|  Remove  |      n       |     n     | n             | n         | n            | log n    |  
## Tree data structures
#### What is a tree
A tree is a hierarchical data structure that consists of nodes connected by edges. Each node in a tree contains references to one or multiple children, with one node designated as the root. The nodes in a tree are organized in such a way that they create a branching structure, where each child node may further contain its own children.
![[NodeTree.excalidraw.svg|700]]
#### Binary trees
Binary trees are a type of tree where each node can have a maximum of two children: a left child and a right child. This constraint makes it relatively easy to operate on the tree, making it suitable for various operations and searches.
![[BinaryTree.excalidraw.svg|700]]
#### Binary search trees
A binary search tree (BST) is a specific type of binary tree where each node follows a particular order or relationship with its children. In a BST, the left child of a node contains elements that are smaller than the node itself, while the right child contains elements that are larger. This ordering property allows for efficient searching and retrieval of elements within the tree.
![[BinarySearchTree.excalidraw.svg|700]]

**Removing elements from a BST can be done in three ways:**

1. **Simple removal:** If the node to be removed has no children, it is simply deleted from the tree.
2. **Replace removal (when the node has one child):** In this case, the node is replaced by its only child, and the link to the parent is adjusted accordingly.
3. **Replace by either the smallest element on the right or by the biggest element on the left:** If the node has two children, it can be replaced by either the smallest element in its right subtree or the largest element in its left subtree. This ensures that the binary search tree properties are maintained.

>[!tip] 3rd type of removal diagram
>![[BinaryTreeRemove3A.excalidraw.svg]]
>![[BinaryTreeRemove3B.excalidraw.svg]]
#### AVL trees
#todo understand the algorithm
AVL trees are binary trees that balance themselves. In AVL trees the height of nodes on the right and left is *roughly equal*. 

>[!important] The AVL tree rule
>**All** nodes in AVL trees follow the following principle: The difference between the height of the left subtree and the left subtree has to be between 1 and -1. This difference is often referred to as the **balance factor**.
>![[AVLTreeBalance1.excalidraw.svg|600]]
>![[AVLTreeBalance2.excalidraw.svg|600]]

##### AVL Tree rotation
>[!info] Left rotation
>![[leftRotation.gif]]

>[!info] Right rotation
>![[rightRotation.gif]]

#todo add rotation cases from photo


## Iterating over trees
#todo add costs from photo 
#explanation recursive functions occupy more space cuz they have their variables stored in stacks 

## Huffman algorithm

## Binary heaps
Binary heaps are specialized binary tree structures with two key properties:

1. **Completeness**: All layers of the tree, except the last one, must be full. This means they should have the maximum number of nodes possible.
2. **Ordering**: In a **max-heap**, the parent node is always greater than its child nodes, while in a **min-heap**, the parent node is always smaller than its child nodes.

>[!info] The height of the heap
> The since all of the layers in the heap (except for the last) are full, we can calculate the height of the heap as $floor(\log_2{n})$ or just $\log{n}$ simplified.

These binary heaps are stored in **arrays**, and the way they are organized in these arrays mimics the structure of the heap itself. It's like building the heap in layers, with the upper layer first, followed by the next, and so on.

This array representation allows for easy navigation between parent and child nodes:

- To move from a child node to its parent node, simply divide the child node's index by 2 and consider only the whole part of the division. This gives you the index of the parent node.
- To move from a parent node to its child nodes, you can reverse the process. Multiply the parent node's index by 2 to find the left child's index, and then add 1 to it to get the right child's index.

>[!attention] 
>In order for this to work the node indexing **must** start at 1. 

### Extracting the Top Element from a Binary Heap

Binary heaps are commonly used for priority queues, where the highest-priority (in the case of a max-heap) or lowest-priority (in the case of a min-heap) element needs to be efficiently retrieved. Extracting the top element is a key operation in this context, and it involves removing the top element while maintaining the heap's structure and ordering.

#### Steps to Extract the Top Element from a Binary Heap

To extract the top element from a binary heap, follow these steps:

1. **Remove the Root Element:** The top element in the heap is always the root of the binary tree. Remove this element from the heap, which creates a gap at the root position.

2. **Replace with the Last Element:** To maintain the completeness property of the heap, replace the removed root element with the last element in the heap's array. This last element will now occupy the root position.

3. **Heapify Down (Sink Down):** After replacing the root with the last element, you need to adjust the heap to ensure the ordering property is preserved. In a max-heap, the new root element should be "sunk down" to the appropriate position. Similarly, in a min-heap, the element should be moved down to its correct position in the heap.

    - For a max-heap, compare the new root with its children. Swap it with the larger child if the larger child is greater than the root, and repeat this process until the root element is in its correct position.

    - For a min-heap, compare the new root with its children. Swap it with the smaller child if the smaller child is smaller than the root, and continue this process until the root element is correctly placed.

This "sink down" process ensures that the heap's ordering property is maintained while preserving the completeness property.
#### Example
![[maxHeapTopDel.gif]]

### Adding Elements to a Binary Heap

Binary heaps are often used for priority queues, where elements with higher or lower priorities need to be efficiently managed. Adding elements to a binary heap is a critical operation to maintain the heap's properties. Here, we'll discuss how to add an element to a binary heap while preserving its structure and ordering.

#### Steps to Add an Element to a Binary Heap

To add an element to a binary heap, follow these steps:

1. **Append the Element:** Add the new element to the end of the array representation of the heap. This maintains the completeness property, as you're adding the element to the next available position in the last layer of the heap.

2. **Heapify Up (Bubble-Up):** After adding the element, you may need to adjust the heap to ensure the ordering property is maintained. In a max-heap, this means that the newly added element should be "bubbled up" the heap until it's in the correct position. Similarly, in a min-heap, the element should be moved up to its appropriate position in the heap.

    - For a max-heap, compare the added element with its parent. If it is larger than its parent, swap the element with its parent and repeat this process until the element is in the correct position.

    - For a min-heap, compare the added element with its parent. If it is smaller than its parent, swap the element with its parent and continue this process until the element is correctly placed.

This "bubble-up" process ensures that the heap's ordering property is maintained while preserving the completeness property.

#### Example
![[addToHeap.gif]]

Adding elements to a binary heap typically has a time complexity of $O(h)$ which can be represented as $O(log{N})$, where N is the number of elements in the heap.

### Heapifying an Array to Create a Binary Heap

In many cases, you may need to convert a regular array of elements into a binary heap, which is a data structure that satisfies the heap properties, including completeness and ordering. This process is known as "heapifying" an array, and it's essential for efficiently performing operations on heaps.

#### Steps to Heapify an Array

To heapify an array to create a binary heap, follow these steps:

1. **Start from the Middle:** The heapify process starts from the middle of the array and moves towards the beginning. This is because elements in the second half of the array are already leaves in the binary tree, and you don't need to perform any operations on them.

3. **Sink Down (Heapify Down):** For each element, perform a "sink down" operation. This means comparing the element with its children (if any) and potentially swapping it with the larger (in a max-heap) or smaller (in a min-heap) child to ensure the ordering property is maintained.
    
    - In a max-heap, if the element is smaller than either of its children, swap it with the larger child. Continue this process until the element is in its correct position.
    
    - In a min-heap, if the element is larger than either of its children, swap it with the smaller child. Repeat this process until the element is correctly placed.
    
3. **Continue Sinking Down:** Continue the "sink down" process for each element in the array, moving towards the beginning of the array.

4. **Array is Now a Binary Heap:** After you've performed the "sink down" operation for all elements, the array is transformed into a binary heap that satisfies the heap properties.

#todo add heap sort using binary heap