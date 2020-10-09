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
