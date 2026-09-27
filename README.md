\# Government Database - BST Assignment



\## 1. Objective



The objective of this assignment is to implement a Binary Search Tree (BST) to organize government identification numbers and compare the performance of BST Search with Linear Search.



The assignment also studies the effect of key length and insertion order on BST height and search performance.



\---



\## 2. Input Data



The following identification numbers are used:



\- A102

\- A25

\- A7

\- B100

\- B12

\- A120

\- B3

\- A45



The identification numbers are treated as strings and compared lexicographically.



\---



\## 3. BST Inorder Traversal



The inorder traversal of the resulting BST is:



A102 A120 A25 A45 A7 B100 B12 B3



\---



\## 4. BST Structure



```text

&#x20;            A102

&#x20;               \\

&#x20;               A25

&#x20;              /   \\

&#x20;           A120    A7

&#x20;                  /  \\

&#x20;                A45  B100

&#x20;                     /

&#x20;                   B12

&#x20;                     \\

&#x20;                      B3



BST Height = 5 edges.



Number of levels = 6.



\---



5\. Search Comparison



Search ID| BST Comparisons| Linear Comparisons

A102| 1| 1

A45| 4| 8

B3| 6| 7

A120| 3| 6

B12| 5| 5

A7| 3| 3

Total| 22| 30

Average| 3.67| 5.00



For the selected search keys, BST required fewer comparisons than Linear Search.



\---



6\. Complexity Analysis



BST Search



\- Best Case: O(1)

\- Average Case: O(log n)

\- Worst Case: O(n)



BST Insertion



\- Best Case: O(1)

\- Average Case: O(log n)

\- Worst Case: O(n)



Linear Search



\- Best Case: O(1)

\- Average Case: O(n)

\- Worst Case: O(n)



Inorder Traversal



\- Time Complexity: O(n)



Space Complexity



\- BST: O(n)

\- Linear Search array: O(n)



For string keys of average length L, comparison cost can add a factor of L.



\---



7\. Effect of Insertion Order



The given insertion order produced a BST with height 5 edges.



For 8 nodes:



\- Best possible height is approximately 3 edges.

\- Worst possible height is 7 edges.

\- Given tree height is 5 edges.



A sorted or reverse-sorted insertion order can create a highly skewed BST.



\---



8\. Effect of Key Length



Key length does not directly determine the height of a BST.



However, longer strings may require more character comparisons.



Therefore, if L is the average key length:



\- Balanced BST: O(L log n)

\- Worst-case BST: O(Ln)

\- Linear Search: O(Ln)



\---



9\. Suitable Approach



For a small database, an ordinary BST can be used.



For a growing database, a self-balancing BST such as an AVL Tree or Red-Black Tree is more suitable because it maintains approximately O(log n) search and insertion performance.



For large database systems, B-Tree or B+ Tree based indexing can also be considered.



\---



10\. Conclusion



The experiment demonstrates the use of a Binary Search Tree for organizing identification numbers. The BST produced fewer total comparisons than Linear Search for the selected search keys.



However, the performance of an ordinary BST depends on its shape and insertion order. A highly skewed BST can degrade to O(n) search time.



Therefore, self-balancing trees are suitable for maintaining efficient searches as the database grows.



\---

