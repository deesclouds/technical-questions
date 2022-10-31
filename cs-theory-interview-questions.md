# CS Theory - Interview Questions

## Questions:

- [x] What is recursion and give an example using Javascript?
- **Explain:** is a technique used to solve problems by creating a function that calls itself until your program achieves the desired result.
- **Use:** to break down complex problems into the smallest solutions.
- **Example:** print numbers to count down to the value to 1.
```
// program to count down numbers to 1
function countDown(number) {
    //display the number
    console.log(number);

    //decrease the number value
    const newNumber = number -1;
    
    //base case
    if (newNumber > 0){
        countDown(newNumber);
    }
}
countDown(4);

[!programiz][https://www.programiz.com/javascript/recursion]
```

- [x] What are types?
- **Explain:** the study of type systems such as integers and strings, depend on practical issues of computer computer architecture, compiler implementation, and language design. can be used as a safety feature, organizational device and a tool for program analysis.
- **Use:** relates to programming languages. can be used for specification and modularization
- **Example:** machine learning-style module is a dependent sum, while polymorphic type can be seen as a dependent product.

- [x] What are data structures?
- **Explain:** used for storing and organizing data. a way of arranging data on a computer to be accessed and updated efficiently.
- **Use:** used for processing, retrieving and storing data.
- **Example:** store a list of items having the same data-type using the array data structure.

- [x] What is an algorithm?
- **Explain:** set of well-defined rules to solve a particular problem that takes in a set of inputs and produces the desired outputs. 
- **Use:** best solution to solve a problem based on data storage to also improve the efficiency of a program.
- **Example:** take two number inputs, add numbers using the '+' operator then displaying the result.

- [x] What is scope / lexical scope in Javascript?
- **Explain:** a scope is a boundary, region or environment.

lexical scope means the value of a function can only be determined by the environment where it was created.
- **Use:** variables can only be called within the block of code in which it was declared/created. to keep our code modular.
- **Example:** 
function getName() {
  const myName = "Oluwatobi";
  return myName;
}
[!lexical/scope][https://dev.to/fleepgeek/i-would-try-to-explain-lexical-scope-in-plain-english-wish-me-luck-4j06]

- [x] What is polymorphism?
- **Explain:** the same function with different signatures called many times. 
- **Use:** use the same method name repeatedly, and reduce the number of functionalities that can be paired together.
- **Example:** three function with the same name and different operations. (inheritance polymorphism)
```
<script>
    class firstClass {
        add() {
            console.log("First Method")
        }
    }
    class secondClass extends firstClass {
        add() {
            console.log(30 + 40);
        }
    }
    class thirdClass extends secondClass {
        add() {
            console.log("Last Method")
        }
    }
    var ob = new firstClass();
    var ob2 = new secondClass();
    var ob3 = new thirdClass();
    ob.add();
    ob2.add();
    ob3.add();
</script>
```
[!polymorphism][https://www.geeksforgeeks.org/polymorphism-in-javascript/?ref=gcse]

- [x] What is encapsulation?
- **Explain:** is a way of restricting access to the inner workings of an object
- **Use:** to hide data members and data functions or methods associated with an instantiated class or object
- **Example:** building a firewall around the class by adding another layer of protection

- [x] What is a Linked List?
- **Explain:** a linear data structure, consists of nodes where each node contains a data field and a reference(link) to the next node in the list.
- **Use:** used for their efficient insertion and deletion and to implement stacks, queues, and other abstact data types
- **Example:** index of(element)- returns the index of a given element if the element is in the list
```
// finds the index of element
indexOf(element)
{
    var count = 0;
    var current = this.head;
 
    // iterate over the list
    while (current != null) {
        // compare each element of the list
        // with given element
        if (current.element === element)
            return count;
        count++;
        current = current.next;
    }
 
    // not found
    return -1;
}
```
[!linkedlist][https://www.geeksforgeeks.org/data-structures/linked-list/]
[!linkedlist-uses][https://brilliant.org/wiki/linked-lists/]

- [x] What is a Doubly Linked List?
- **Explain:** similar to a singly linked list, it is a data structure that consists of notes.
- **Use:** easier to implement than a singly linked list
- **Example:**
shift(removing a node from the beginning)
```
shift() {
  if (this.length === 0) return undefined;
  const temp = this.head;
  if (this.length === 1) {
    this.head = null;
    this.tail = null;
  } else {
    this.head = temp.next;
    this.head.prev = null;
    temp.next = null;
  }
  this.length--;
  return temp;
}
```
[!doubly linked list][https://javascript.plainenglish.io/doubly-linked-lists-with-javascript-9c20a9dc4fb3]

- [x] What is a Queue?
- **Explain:** defined as a linear data structure that is open at both ends and the operations are performed in First In First Our (FIFO) order.
- **Use:** to handle multiple data, fast and flexible can be 
- **Example:**
waiting in line and execute time after time.
[!queue][https://www.geeksforgeeks.org/queue-data-structure/?ref=gcse]

- [x] What is a Stack?
- **Explain:** linear data structure which addition or removal of element follows LIFO ( last in first out) and FILO (first in last out)
- **Use:**
- **Example:**
[!stack][https://www.geeksforgeeks.org/implementation-stack-javascript/]

- [x] What is a Hash Table?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is a Heap?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is a Trie?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is a Tree?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is a Binary Search Tree?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is a Disjoing Set?
- **Explain:**
- **Use:**
- **Example:**

- [x] What is a Bloom Filter?
- **Explain:**
- **Use:**
- **Example:**

- [x] Demonstrate Bubble Sort and explain when you might use it?
- **Explain:**
- **Use:**
- **Example:**

- [x] Demonstrate Insertion Sort and explain when you might use it?
- **Explain:**
- **Use:**
- **Example:**

- [x] Demonstrate Merge Sort and explain when you might use it?
- **Explain:**
- **Use:**
- **Example:**

- [x] Demonstrate Quicksort and explain when you might use it?
- **Explain:**
- **Use:**
- **Example:**













