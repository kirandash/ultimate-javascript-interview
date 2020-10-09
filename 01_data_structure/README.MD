# M1 Data Structure
## M1.1 Intro to Data Structure
### M1.1.1 What is Data Structure
1. What is Data Structure
    * A way of **organizing** data that is stored in a computer or database
    * Many different types of data structures
    * Each type of data structure represents a different way of **organzing** the data

2. Why do we have different types of Data structures?
    * They all have different strengths and weaknesses
    * Some are fast at **storing** and **recording** data, while others are not
    * Some are fast at **searching** and **retrieving** data, while others are not

3. Why are data structures important to know?
    * Can have big impact on how **performant**, **quick** and **efficiently** a program runs.
    * Ex: Linked Lists are better when it comes to storing while hash tables are better when it comes to search.
    * Reinforce knowledge of JS algorithms and concepts. viz: constructor funcs, recursion, this keyword, prototype object, Big O notation

### M1.1.2 constructor functions and the this keyword
1. Constructor fns are used to create new JS objects. this keyword always refers to its context

### M1.1.3 The Prototype Object
1. Every Object as a Prototype object by default. Any properties that are added to Prototype object will be automatically be inherited to all instances.

## M1.2 Linked Lists
### M1.2.1 What is a Linked List
1. A list of nodes connected together through a fine line.
    - **Singly Linked List**: Each node has reference only to the next node.
    - **Doubly Linked List**: Each node has reference to the next and prev node as well.
    - Note: First node is called the **head** pointer of the linked list. Last node is called the **tail** pointer of the linked list.
    - Task: Add a node to head or tail of linked list. Search through linked list.
    - Ex: JSON object: { value: 7, next: nextNode, prev: prevNode }

### M1.2.2 Linked List and Node constructor functions
1. To go through a Linked List all we need is:
    - head pointer
    - tail pointer
2. Since each node has info about prev and next node: we can easily go through the linked lists.

### M1.2.3 Add To Head - LL method
1. Create addToHead method for LL prototype

### M1.2.4 Add node to head of LL
1. Must take care of two scenarios while adding the new node to the head linked list:
    - If LL is empty: point head and tail to same node
    - If the LL has any entries: point new head and old head to correct points
        * Point current head node's prev to new node being added. Earlier it was pointing to null

### M1.2.5 Using add to head

### M1.2.6 Add To Tail - LL prototype method
1. If LL is not empty - current tail nodes next must not point to null any more and must point to the new node

### M1.2.7 Test Add To Tail and Add To Head

### M1.2.8 Remove Head
1. If LL is not empty and if LL is empty

### M1.2.9 Remove Tail

### M1.2.10 Search LL

### M1.2.11 Add indexOf

### M1.2.12 Big O Notation and Calculating the Runtime of a Fn
1. Big O notation helps us analyze the complexity of an algorithm and tells us how perfomant the code will be
2. It tells us how slower our code will get if we add more data
3. All possible cases:
    - 1. **Constant Run Time** - If we increase the size of data - execution time does not change: Big O Notation: O(1)
    - 2. **Lineaer Run Time** - Big O Notation: O(n) - Ex: for loop
    - 3. **Exponential Run Time** - Big O Notation: O(n^2) - Ex: for loop in for loop - Not very efficient when data becomes large
    - 4. **Logarithmic Run Time** - Big O Notation: O(log n) - Ex: Binary search - Very performant when it comes to handling large data
        - Ex: 4000 element will take only 12 operations to find
4. Binary Search: Binary search are always done on sorted arrays.

### M1.2.13 Linked List - Performance Analysis
1. Performance:
    * Add/remove: Constant Time O(1) 
        - Add/remove head
        - Add/remove tail
    * Searching Through Linked List
        - Linear time complexity O(n)
        - O(n)
    *  LL are quite performant and commonly used DS
    *  Practical use
        - Online gaming
        - Poker, board games, dominoes
2. Interview Question: What are memory management benefits of Linked Lists?
Ans: **Memory Management Benefits:**
    - Data doesn't have to be stored together
    - Data can be stored in separate chunks in separate places yet still be linked with next and prev pointer.

## M1.3 Binary Search Tree
### M1.3.1 What is a binary Search tree
1. A binary search tree is also a collection of nodes. Where each node has it's own value and is connected to two more nodes.
    - Each left node < parent node. Each right node > parent node
    - when we add a new node, we start from the top and move our way down by calculating the > or < logic and insert the new node when a new empty slot is found.
    - Each node in tree itself is a BST
2. Topics
    - BST - create root node, insert nodes
    - Contains
    - Traversal
        * **Depth First Traversal**: Start from top and go all the way to the bottom on left and then on right.
        * **Breadth First Traversal**: Start from top and go down level by level.

### M1.3.2 Recursion
1. We need to understand the concept of recursion bcoz BSTs are recursive.
2. Recursion is **when a fn calls itself**.
3. All recursive fn basically has 2 cases:
    * **base case**: in which the fn doesn't call itself and does some other task
    * **recursive case**: in which the fn calls itself
4. Keep calling it self until the base case satisfies is called recursion.
5. Ex: Factorial of a num

### M1.3.3 Insert Method - BST
1. Each BST is defined by: value, left child and right child
2. **Steps**:
    - if value is less than parent node value - insert it to left
        * if there is no left child - add new BST to left
        * is there already a left child - recursively call insert function on its left
    - if value is > parent node value - insert it to right
        * if there is no right child - add new BST to right
        * if there is there already a right child - recursively call insert function on its right

### M1.3.4 Contains Method
1. To check if BST contains a value

### M1.3.5 Depth First Traversal
1. On left go all the way till last element and then go up and right to next branch and then again all the way to left down. then up and next right branch.
2. Usees powerful recursive approach

### M1.3.6 Refactoring Depth First Traversal to support orders
1. So far Depth First traversal is implemented in order. We will configure it to have different orders now
    - in order: left children ---> parent node ---> right children
    - pre order: parent node ---> left children ---> right children (application: when we make copy of a tree)
    - post order: left children ---> right children ---> parent node

### M1.3.7 Breadth First Traversal
1. Moving down the tree level by level
2. Application:
    - Define a heirarchy or level of commands. Ex: Structure of a company

### M1.3.8 Exercise Add methods for getMinVal and getMaxVal
1. getMinVal - min value must be found at the furthest left child
2. getMaxVal - max value must be found at the furthest right child

### M1.3.9 Performance and application
1. BSTs are used often to store data.
2. Fast to searc and retrieve data from.
3. also fast to add/remove
4. Big O notation: O(log n): logarithmic run time. as we only search for half of the data set.
    - faster than linked list. (O (n)) - might have to search through all nodes. Ex: 4000 nodes
    - But in balanced BST, we have to search only 12 times in 4000 nodes
5. Cons: 
    - For specific data set: we might end up having imbalanced BST ex: a tree with only right nodes or only left nodes. Then the search will be similar to LL.
6. Note: BSTs are more performant when they are **balanced**
7. Application: Anything that needs a binary search
    - Ex: dictionary, phone book, users etc
