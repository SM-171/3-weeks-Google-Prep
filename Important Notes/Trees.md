## Important Things to Remember
1) Bitwise operation for finding 2^h is **1<<h**.

2) For a complete binary tree, time complexity for any traversal (inorder, preorder...) is **0(N)**. Since, the max height(h) of a complete binary tree is logN, auxiliary space complexity is **O(logN)**.


## Binary Search Trees
A **valid BST** is defined as follows:

- The left subtree of a node contains only nodes with keys less than the node's key.
- The right subtree of a node contains only nodes with keys greater than the node's key.
- Both the left and right subtrees must also be binary search trees.

1) By convention, we do not consider any case of duplication.
NOTE: Ask as a follow-up question "if duplicates are allowed".
If duplicates are allowed, we can use freq map [node, freq].

2) Why we need BST?
- Generally the height of a BST is **O(logN) {base = 2}**. Thus, searching for any number in a BST will have a TC of **O(logN)** while, in a linear data structure or skew binary tree it will be **O(N)**.


## Important Questions

1) [Vertical Order Traversal](https://leetcode.com/problems/vertical-order-traversal-of-a-binary-tree/description/)
- Data structures: priority_queue and unordered_map

2) [Maximum Width of Binary Tree](https://leetcode.com/problems/maximum-width-of-binary-tree/description/)
- This question is simple but requires handling of integer overflow
- Revise to go over over-flow handling.

3) [Amount of time for BT to be infected](https://leetcode.com/problems/amount-of-time-for-binary-tree-to-be-infected/description/)

4) [Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/)
NOTE: Variation for BST - [Maximum Path Sum BST](https://leetcode.com/problems/maximum-sum-bst-in-binary-tree/)
- Good question to revise recursion in BTs

5) [BT to Linked List](https://leetcode.com/problems/flatten-binary-tree-to-linked-list/)
- Revise all 3 methods as mentioned in [video](https://www.youtube.com/watch?v=sWf7k1x9XR4&list=PLkjdNRgDmcc0Pom5erUBU4ZayeU9AyRRu&index=38)

6) [Serialise and Deserialise Tree](https://leetcode.com/problems/serialize-and-deserialize-binary-tree/description/)
- Very good question to practice how to use "stringstream" in C++
