# 0x1D. C - Binary trees

This repository contains the solutions to the tasks of the "0x1D. C - Binary trees" project at ALX.

## Learning Objectives

- What is a binary tree
- What is the difference between a binary tree and a binary search tree
- What is the possible gain in terms of time complexity compared to linked lists
- What are the depth, the height, the size of a binary tree
- What are the different traversal methods to go through a binary tree
- What is a complete, a full, a perfect, a balanced binary tree

## Requirements

- All the files will be compiled on Ubuntu 14.04 LTS
- Programs and functions will be compiled with gcc 4.8.4 using the flags -Wall -Werror -Wextra and -pedantic
- All the header files are located in the `./inc` folder
- All the provided code is based on the `bst.h` binary tree header file
- Do not include any kind of main function in any of the files inside the `./src` folder
- All the files inside `./src` will be compiled to generate a `libhbtn.a` library

## Tasks

### [0. New node](./0-binary_tree_node.c)

Function that creates a new Node in a Binary Tree:

- Prototype: `binary_tree_t *binary_tree_node(binary_tree_t *parent, int value);`
- Where parent is a pointer to the parent node of the node to create
- And value is the value to put in the new node
- The function must return a pointer to the new node, or NULL on failure

### [1. Insert left](./1-binary_tree_insert_left.c)

Function that inserts a node as the left-child of another node in a Binary Tree:

- Prototype: `binary_tree_t *binary_tree_insert_left(binary_tree_t *parent, int value);`
- Where parent is a pointer to the node to insert the left-child in
- And value is the value to store in the new node
- The function must return a pointer to the created node, or NULL on failure or if parent is NULL
- If parent already has a left-child, the new node must take its place, and the old left-child must be set as the left-child of the new node.

### [2. Insert right](./2-binary_tree_insert_right.c)

Function that inserts a node as the right-child of another node in a Binary Tree:

- Prototype: `binary_tree_t *binary_tree_insert_right(binary_tree_t *parent, int value);`
- Where parent is a pointer to the node to insert the right-child in
- And value is the value to store in the new node
- The function must return a pointer to the created node, or NULL on failure or if parent is NULL
- If parent already has a right-child, the new node must take its place, and the old right-child must be set as the right-child of the new node.

### [3. Delete](./3-binary_tree_delete.c)

Function that deletes an entire Binary Tree:

- Prototype: `void binary_tree_delete(binary_tree_t *tree);`
- Where tree is a pointer to the root node of the tree to delete
- If tree is NULL, do nothing

### [4. Is leaf](./4-binary_tree_is_leaf.c)

Function that checks if a node in a Binary Tree is a leaf:

- Prototype: `int binary_tree_is_leaf(const binary_tree_t *node);`
- Where node is a pointer to the node to check
- The function must return 1 if node is a leaf, otherwise 0
- If node is NULL, return 0

### [5. Is root](./5-binary_tree_is_root.c)

Function that checks if a given node is a root in a Binary Tree:

- Prototype: `int binary_tree_is_root(const binary_tree_t *node);`
- Where node is a pointer to the node to check
- The function must return 1 if node is a root, otherwise 0
- If node is NULL, return 0

### [6. Pre-order traversal](./6-binary_tree_preorder.c)

Function that goes through a Binary Tree using pre-order traversal:

- Prototype: `void binary_tree_preorder(const binary_tree_t *tree, void (*func)(int));`
- Where tree is a pointer to the root node of the tree to traverse
- And `func` is a pointer to a function to call for each node. The value in the node must be passed as a parameter to this function.
- If `tree` or `func` is NULL, do nothing

### [7. In-order traversal](./7-binary_tree_inorder.c)

Function that goes through a Binary Tree using in-order traversal:

- Prototype: `void binary_tree_inorder(const binary_tree_t *tree, void (*func)(int));`
- Where `tree` is a pointer to the root node of the tree to traverse
- And `func` is a pointer to a function to call for each node. The value in the node must be passed as a parameter to this function.
- If `tree` or `func` is `NULL`, do nothing

### [8. Post-order traversal](./8-binary_tree_postorder.c)

Function that goes through a Binary Tree using post-order traversal:

- Prototype: `void binary_tree_postorder(const binary_tree_t *tree, void (*func)(int));`
- Where `tree` is a pointer to the root node of the tree to traverse
- And `func` is a pointer to a function to call for each node. The value in the node must be passed as a parameter to this function.
- If `tree` or `func` is `NULL`, do nothing

### [9. Height](./9-binary_tree_height.c)

Function that measures the height of a Binary Tree:

- Prototype: `size_t binary_tree_height(const binary_tree_t *tree);`
- Where `tree` is a pointer to the root node of the tree to measure the height
- The function must return the height of the tree, or 0 if `tree` is `NULL`
- A tree with a single node has a height of `0`
- If `tree` is `NULL`, the function must return `0`

### [10. Depth](./10-binary_tree_depth.c)

Function that measures the depth of a node in a Binary Tree:

- Prototype: `size_t binary_tree_depth(const binary_tree_t *tree);`
- Where `tree` is a pointer to the node to measure the depth
- The function must return the depth of the node, or 0 if `tree` is `NULL`
- A node at the root of a tree has a depth of `0`
- If `tree` is `NULL`, the function must return `0`

### [11. Size](./11-binary_tree_size.c)

Function that measures the size of a Binary Tree:

- Prototype: `size_t binary_tree_size(const binary_tree_t *tree);`
- Where `tree` is a pointer to the root node of the tree to measure the size
- The function must return the size of the tree, or 0 if `tree` is `NULL`
- A tree with a single node has a size of `1`
- If `tree` is `NULL`, the function must return `0`

### [12. Leaves](./12-binary_tree_leaves.c)

Function that counts the leaves in a Binary Tree:

- Prototype: `size_t binary_tree_leaves(const binary_tree_t *tree);`
- Where `tree` is a pointer to the root node of the tree to count the number of leaves
- The function must return the number of leaves in the tree, or 0 if `tree` is `NULL`
- A node is a leaf if it has no children
- If `tree` is `NULL`, the function must return `0`

### [13. Nodes](./13-binary_tree_nodes.c)

Function that counts the nodes with at least 1 child in a Binary Tree:

- Prototype: `size_t binary_tree_nodes(const binary_tree_t *tree);`
- Where `tree` is a pointer to the root node of the tree to count the number of nodes with at least 1 child
- The function must return the number of nodes with at least 1 child in the tree, or 0 if `tree` is `NULL`
- A NULL pointer is not a node
- If `tree` is `NULL`, the function must return `0`

### [14. Balance factor](./14-binary_tree_balance.c)

Function that measures the balance factor of a Binary Tree:

- Prototype: `int binary_tree_balance(const binary_tree_t *tree);`
- Where `tree` is a pointer to the root node of the tree to measure the balance factor
- The function must return the balance factor of the tree, or `0` if `tree` is `NULL`
- The balance factor is calculated as the difference between the height of the right subtree and the height of the left subtree
- If a node has only a left child, the height of the right subtree is considered to be `0`
- If a node has only a right child, the height of the left subtree is considered to be `0`
- If `tree` is `NULL`, return `0`

### [15. Is full](./15-binary_tree_is_full.c)

Function that checks if a Binary Tree is full:

- Prototype: `int binary_tree_is_full(const binary_tree_t *tree);`
- Where `tree` is a pointer to the root node of the tree to check
- The function must return `1` if `tree` is a full Binary Tree, `0` otherwise
- If `tree is `NULL`, the function must return `0`

A full binary tree is a tree in which every node has either 0 or 2 children nodes.

### [16. Is perfect](./16-binary_tree_is_perfect.c)

Function that checks if a Binary Tree is perfect:

- Prototype: `int binary_tree_is_perfect(const binary_tree_t *tree);`
- Where `tree` is a pointer to the root node of the tree to check
- The function must return `1` if `tree` is a perfect Binary Tree, `0` otherwise
- If `tree` is `NULL`, the function must return `0`

A perfect binary tree is a tree in which all interior nodes have two children and all leaves have the same depth or same level.

### [17. Sibling](./17-binary_tree_sibling.c)

Function that finds the sibling of a node in a binary tree:

- Prototype: `binary_tree_t *binary_tree_sibling(binary_tree_t *node);`
- Where `node` is a pointer to the node to find the sibling
- The function must return a pointer to the sibling node
- If `node` is `NULL`, the function must return `NULL`
- If `node` has no sibling, the function must return `NULL`

### [18. Uncle](./18-binary_tree_uncle.c)

Function that finds the uncle of a node in a binary tree:

- Prototype: `binary_tree_t *binary_tree_uncle(binary_tree_t *node);`
- Where `node` is a pointer to the node to find the uncle
- The function must return a pointer to the uncle node
- If `node` is `NULL`, the function must return `NULL`
- If `node` has no uncle, the function must return `NULL`

The uncle is the sibling of the parent node.

### [100. Heap insert](./100-binary_tree_heap_insert.c)

Function that inserts a value in Max Binary Heap:

- Prototype: `heap_t *binary_tree_heap_insert(heap_t **root, int value);`
- Where `root` is a double pointer to the root node of the Heap to insert the value
- And `value` is the value to store in the node to be inserted
- The function must return a pointer to the inserted node, or `NULL` on failure
- If `root` is `NULL`, the created node must become the root node.
- You have to respect a `Max Heap` ordering

### [101. Heap extract](./101-binary_tree_heap_extract.c)

Function that extracts the root node of a Max Binary Heap:

- Prototype: `int binary_tree_heap_extract(heap_t **root);`
- Where `root` is a double pointer to the root node of the heap to extract the top value
- The function must return the value stored in the root node
- The root node must be freed and replace with the last level-order level node of the heap tree.
- Once replaced, the heap tree must be rebuilt if necessary
- If `root` is `NULL`, the function return `0`

### Note

You are not allowed to use the global variable `stdout`.

## Binary Trees

A binary tree is a tree where each node has at most two children, left and right. Binary trees are used to implement binary search trees, heaps, and expression trees. 

### Data Structure

The following is the basic structure of a binary tree node:
```c
typedef struct binary_tree_s {
    int n;
    struct binary_tree_s *parent;
    struct binary_tree_s *left;
    struct binary_tree_s *right;
} binary_tree_t;
```

### Traversing

There are three ways to traverse a binary tree:

- **In-order traversal**: visits first the left subtree, then the root, then the right subtree.
- **Pre-order traversal**: visits first the root, then the left subtree, then the right subtree. 
- **Post-order traversal**: visits first the left subtree, then the right subtree, then the root.

### Installing

To use the functions in your C code, you have to clone the repository and include the header file `binary_trees.h` in your code:

```c
#include "binary_trees.h"
```
### Usage

Here is an example of a complete program that uses our binary tree functions to create and print a binary tree:

```c
#include <stdio.h>
#include "binary_trees.h"

int main(void)
{
    binary_tree_t *tree;

    tree = binary_tree_node(NULL, 98);
    tree->left = binary_tree_node(tree, 12);
    tree->right = binary_tree_node(tree, 402);
    tree->left->right = binary_tree_node(tree->left, 54);
    tree->right->left = binary_tree_node(tree->right, 128);
    tree->right->right = binary_tree_node(tree->right, 256);

    binary_tree_print(tree);

    return (0);
}
```
