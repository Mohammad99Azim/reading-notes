# Tree

### Depth First

There are multiple ways to carry out depth first traversal

- Pre-order:  ``root >> left >> right``
- In-order:   ``left >> root >> right``
- Post-order: ``left >> right >> root``


#### Pre-order
the pre order is to start from the root  then go to the left of the tree then in the end go to the right

and this is the code how to print the values in the tree based on the pre-order

```
def preOrder(root)

  print(root.value)

  if root.left is not NULL:
      preOrder(root.left)

  if root.right is not NULL:
      preOrder(root.right)
      
```


#### In-order

the In order is to start from the left  then go to the root of the tree then in the end go to the right

and this is the code how to print the values in the tree based on the In-order

```
def inOrder(root):

    if root.left is not NULL:
        inOrder(root.left)

    print(root.value)

    if root.right is not NULL:
        inOrder(root.right)
        
```


#### Post-order

````
def postOrder(root)


    if root.left is not NULL:
        postOrder(root.left)

    if root.right is not NULL:
        postOrder(root.right)

    print(root.value)
    
````


### Breadth First


Breadth first traversal iterates through the tree by going through each level of the tree node-by-node. 




### Binary Tree Vs K-ary Trees

Binary Trees restrict the number of children to two (hence our ``left`` and ``right`` children).

K-ary Tree can have any number of children per node




### Binary Search Trees

In a BST, nodes are organized in a manner where all values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right.


Searching a BST can be done quickly, because all you do is compare the node you are searching for against the root of the tree or sub-tree. If the value is smaller, you only traverse the left side. If the value is larger, you only traverse the right side.


**Big O**

In an unbalanced tree, the worst case height of the tree is O(n). but in the balanced tree is log(n) becase every loop we tack half of the node that we have 














