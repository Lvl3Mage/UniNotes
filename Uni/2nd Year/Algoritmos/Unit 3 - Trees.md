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

**Removing elements from a BST can be done in three ways:**

1. **Simple removal:** If the node to be removed has no children, it is simply deleted from the tree.
2. **Replace removal (when the node has one child):** In this case, the node is replaced by its only child, and the link to the parent is adjusted accordingly.
3. **Replace by either the smallest element on the right or by the biggest element on the left:** If the node has two children, it can be replaced by either the smallest element in its right subtree or the largest element in its left subtree. This ensures that the binary search tree properties are maintained.

>[!tip] 3rd type of removal diagram
>![[BinaryTreeRemove3A.excalidraw.svg]]
>![[BinaryTreeRemove3B.excalidraw.svg]]
#### AVL trees
#todo understand the algorithm