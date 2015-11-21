# mastering-algorithm
Book notes for C programming, book: mastering algorithm in C

## Chapter 8: Hash Table
Def: Hash table consists of an array in which data is accessed via a special index called key.
* establish mapping between the set of all possible keys and positions.
* used to perform constant time searches.


## Chapter 9: Trees
Each node in a binary tree contains three parts: a data member and two pointers(left and right)
If no child, then set the appropriate pointer to NULL. 

1. Traversal Methods: visiting its nodes one at a time in a specific order.
* Four types: preorder, inorder, postorder, level order.
* Preorder: root, left, right
* Inorder: left, root, right
* Postorder: left, right, root
* Level-order: visit by level, root, left to right on same level


2. Interface for Binary Trees
* Initializes the binary tree spcefied by tree.
```
void bitree_init (BiTree *tree, void(*destroy)(void *data))
```

* Destroy the binary tree specified by tree
```
void bitree_destroy(BiTree *tree)
```

* Insert a node as the left child of node. If node is NULL, new node is inserted as root node. 0 if successful, -1 otherwise.
```
int bitree_ins_left(BiTree *tree, BiTreeNode *node, const void *data)
```

* insert on right
```
int bitree_ins_right(BiTree *tree, BiTreeNode *node, const void *data)
```

* Remove subtree rooted as left child of node
```
void bitree_rem_left(BiTree *tree, BiTreeNode *node)
```

* Merge two binary trees specified by left and right into the single binary tree merge.
```
int bitree_merge(BiTree *merge, BiTree *left, BiTree*right, const void *data)
```

* Number of nodes in the tree
```
int bitree_size(const BiTree *tree)
```

* Node at the root of tree
```
BiTreeNode *bitree_root(const BiTree *tree)
```

* 1 if node marks end of branch, 0 otherwise
```
int bitree_is_eob(const BiTreeNode *node)
```

* 1 if the node is a leaf node, 0 otherwise
```
int bitree_isleaf(const BiTreeNode *node)
```

* Data stored in the node
```
void *bitree_data(const BiTreeNode *node)
```

* Left/right child of specific node
```
BiTreeNode *bitree_left(const BiTreeNode *node)
```


