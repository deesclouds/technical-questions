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
[!types][]
- [x] What are data structures?
- **Explain:** used for storing and organizing data. a way of arranging data on a computer to be accessed and updated efficiently.
- **Use:** used for processing, retrieving and storing data.
- **Example:** store a list of items having the same data-type using the array data structure.
[!data structures][]
- [x] What is an algorithm?
- **Explain:** set of well-defined rules to solve a particular problem that takes in a set of inputs and produces the desired outputs. 
- **Use:** best solution to solve a problem based on data storage to also improve the efficiency of a program.
- **Example:** take two number inputs, add numbers using the '+' operator then displaying the result.

- [x] What is scope / lexical scope in Javascript?
- **Explain:** a scope is a boundary, region or environment.
[!algorithm][]
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
- **Explain:** defined as a linear data structure that is open at both ends and the operations are performed in First In First Out (FIFO) order.
- **Use:** to handle multiple data, fast and flexible can be 
- **Example:**
Waiting in line and execute time after time. Think of a song queue. 
[!queue][https://www.geeksforgeeks.org/queue-data-structure/?ref=gcse]

- [x] What is a Stack?
- **Explain:** linear data structure which addition or removal of element follows LIFO ( last in first out) and FILO (first in last out)
- **Use:** Done using arrays and linked lists where the top position is tracked using a variable or header pointer respectively.
- **Example:**
Opposite of restaurant procedure. Think of placing foods items on shelf. Old items go in the back and the newer items in the front. 
[!stack][https://www.geeksforgeeks.org/implementation-stack-javascript/]
[!stack][https://www.techopedia.com/definition/9523/stack]

- [x] What is a Hash Table?
- **Explain:** also called hash map. a data structure that maps keys to values. 
- **Use:** map the value of indexes in an array
- **Example:**listing the values within stored positions within the array or hash table
[!hash table][https://www.freecodecamp.org/news/hash-tables/]
[!hash table][https://www.geeksforgeeks.org/hashing-data-structure/?ref=gcse]

- [x] What is a Heap?
- **Explain:** special Tree-based data structure in which the tree is a complete binary tree
- **Use:** to construct a priority queue. it's one of the fastest sorting algorithms.
- **Example:** think of multiplication refactoring trees
[!heap][https://www.geeksforgeeks.org/heap-data-structure/?ref=gcse]

- [x] What is a Trie?
- **Explain:** a data structure whose nodes store the letters of an alphabet
- **Use:** a special data structure used to store stings that can be visualized like a graph
- **Example:** A trie for keys "A", "to", "tea", "ted", "ten", "i", "in", and "inn"
[!trie][https://www.hackerearth.com/practice/data-structures/advanced-data-structures/trie-keyword-tree/tutorial/]

- [x] What is a Tree?
- **Explain:** a collection of entities called nodes. nodes are connected by edges. first node is called the root
- **Use:** organize data hierarchically 
- **Example:** databases, ie. github branches
[!tree][https://www.freecodecamp.org/news/all-you-need-to-know-about-tree-data-structures-bceacb85490c/]

- [x] What is a Binary Search Tree?
- **Explain:** allows for fast insertion, removal, and lookup of items while offering an efficient way to iterate them in sorted order.
- **Use:** for searching algorithms
- **Example:** A Self-Balancing Binary Search Tree used to maintain sorted stream of data. Suppose we are getting online orders placed and we want to maintain the live data (in RAM) in sorted order of prices. 
[!binary search tree][https://www.geeksforgeeks.org/applications-of-bst/]

- [x] What is a Disjoint Set?
- **Explain:** two sets are called disjoint sets if they don't have any element in common, the in
- **Use:** 
Use Cases of Dis-joint set Data Structure
1)It is used to keep track of connected component in an undirected graph. 2)It is used to detect cycles in the graph. 3)It is used to calculate the minimum spanning tree in Kruskal's algorithm. 4)It is used in Maze generation problems.
- **Example:** 
[!disjoint][https://www.geeksforgeeks.org/disjoint-set-data-structures/]
[!disjoing][https://www.oodlestechnologies.com/blogs/understanding-disjoint-set-and-their-use-cases-in-computer-science/]

- [x] What is a Bloom Filter?
- **Explain:** space-efficient probabilistic data structure 
- **Use:** to test whether an element is a member of a set.
- **Example:**checking availability of username is a set membership problem, where the set is the list of all registered username.
[!boom filter][https://www.geeksforgeeks.org/bloom-filters-introduction-and-python-implementation/]
- [x] Demonstrate Bubble Sort and explain when you might use it?
- **Explain:** the simplest sorting algorithm that works by repeatedly swapping the adjacent elements if they are in the wrong order.
- **Use:** to sort small data sets in ascending and descending order
- **Example:** a bubble sort algorithm is how the contact list on your phone is sorted in alphabetical order
[!bubble sort][https://www.geeksforgeeks.org/bubble-sort/]
[!bubble sort][https://www.indeed.com/career-advice/career-development/bubble-sorting]

- [x] Demonstrate Insertion Sort and explain when you might use it?
- **Explain:**  simple sorting algorithm that sorts an array one item at a time. 
- **Use:** sort items in ascending order based off their key value. works similar to the way you sort playing cards in your hands.
- **Example:** One more real-world example of insertion sort is how tailors arrange shirts in a cupboard, they always keep them in sorted order of size and thus insert new shirts at the right position very quickly by moving other shirts forward to keep the right place for a new shirt.
[!insertion sort][https://javarevisited.blogspot.com/2014/12/insertion-sort-algorithm-in-java-to-array-example.html]
[!insertion sort][https://www.geeksforgeeks.org/insertion-sort/]
[!insertion sort][https://www.geeksforgeeks.org/insertion-sort/#:~:text=Basically%2C%20Insertion%20sort%20is%20efficient,which%20are%20already%20partially%20sorted]

- [x] Demonstrate Merge Sort and explain when you might use it?
- **Explain:** sorting algorithm based on the divide and conquer paradigm. the array is initially divided into two equal haves and then they are combined in a sorted manner.
- **Use:** 
- **Example:**

- [x] Demonstrate Quicksort and explain when you might use it?
- **Explain:**
- **Use:**
- **Example:**













