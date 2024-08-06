

## Array:     
Array to store list of numbers, strings or any items         
It is linear data structure and store in sequential manner in memory, and can get by index number.     

### Static Array: java has static array,       
Dynamic Array: by default, javascript has dynamic array, in java its vector and Arraylist, vector grow 100% and array list grow 50% means if you create a new array using vector, 4 previous and 4 new space(8 total), so it will be double than previous array. And array list will add 2 more (total 6)      

### Time Complexity:      
1- Lookup/search/find by index = O(1)      
2- Insert Item in static array: O(n) because firs the copy elements of the previous array into new array, then insert a new element        
3- Delete Item in last: It will take O(1) but it is best case scenario, the worst case scenario is it can be in the start of the array, then we have to remove it and then shift all the item one item back to fill the first space, its O(n)          

 - - - - - - - - - - - -  



## Linked List:

Linked List is a linear data structure, in which elements are not stored at a contiguous location, rather they are linked using pointers. 
Linked List forms a series of connected nodes, where each node stores the data and the address of the next node. Each node points/refernce to the next node. Because they are linked together, First node is called Head and last node is called Tail.
Nodes will store anywhere in the memory where they get space.


Time (Run time) Complexity of operations in Linked List: (Big O notation)

### 1- Lookup(find) by Value: O(n)
To find the value in the linked list, we have to traverse through all the linked list, In worst case, the value may be stored in the last node, so the operations can be O(n)

### 2- Find By Index:
We don’t have index in linked list because the values are stored all over the memory, each node has the address of the next node, they are not next to each other. So still we have to traverse all the linked list in worst case scenario, so it will be O(n)

### 3- Inserting Element 
1- At the End:  simply need to create a node, In the tail, we have to store the address of it and then remove the tail from there and reference the tail to this new node - O(1)
2- At the beginning: we have reference to the head which is our first node.  simply create a new node, link it to the first node and then remove the head from that node and reference to this node. - O(1)
3- In the middle: First we have to find a node which in O(n) operation and then delete the node which is O(1) operation, which means mainly its O(n) operations.

### 4- Deleting Elements:
#### 1- From the Beginning: O(1) operation
  Deleting from the beginning is so fast, set the Head from the first node to the 2nd node - so mainly its a O(1) operation (we should also remove the link to the first node, because if we will not remove it the garbage collector will think, it is still in use so it will not remove the node)

#### 2- From the End: O(n) operation.
 Its little tricky, we have tail at last node, but it don’t have address fro the previous node, so to reach out to the node which is before the last node, we have to traverse all the linked list till 2nd last node and then move the tail to the 2nd last node and remove the link also- so we have to traverse the linked list it is O(n) operation.

#### 3- From the Middle: O(n) operation.
  so first we have to traverse all the values to find the desired node, then just change the reference of previous node to the next node of desired value. For example we want to remove the 3rd item, then we just have to change the address stored in 2nd item and store the address of 4th item and also remove the link of third node. In this way, it will be removed by garbage collector from the memory. - It is O(n) operation.

  - - - - - - - - - - - - - - - - 


## Stack :
A Stack is a linear data structure that holds a linear, ordered sequence of elements. It follows LIFO principles, first in last out , the element that was inserted last will be removed first.

### Implementation:
1- It implement the undo feature
2- Build compilers (e.g. syntax checking)
3-  Evaluate expression (eg 1 + 2  * 3 ) 
4- Build navigation (eg forward/back) (web browser and apps has forward and back button to go previous or forward pages)

### Stack operations:
push(item) => which push/insert the item on the top
Pop() =>  removes the item from the top
Peek() => returns the top item with our removing it from the stack
isEmpty() => 

### Run time complexity:
Isempty and peek operation run with O(1)
Pop and push also runs on O(1) because we can easily add or remove last item in linked list and in Array.

 - - - - - - - - - - - - 

## Queues:
Queue follow FIFO(first in first out) principle where what ever is entered first in queue that is processed first,     
A queue is a linear data structure where elements are stored in the FIFO (First In First Out) principle where the first element inserted would be the first element to be accessed. A queue is an Abstract Data Type (ADT) similar to stack, the thing that makes queue different from stack is that a queue is open at both its ends. The data is inserted into the queue through one end and deleted from it using the other end. Queue is very frequently used in most programming languages.      
Queue uses two pointers − front and rear    

#### Application software queues are 
Printer    
Operating systems    
Live Support System    
Web servers    
Wherever we process a jobs based on order we received them.     


#### Operations:
Enqueue: adding an item to the back of the queue     
Dequeue: moving an item at the front of the queue     
Peek : for getting the item at the front without removing it     
isEmpty:     
isFull      

These are operations take O(1) constant time because items are added or removed from the end so it is fast.

 - - - - - - - - - - - 

  
### Hash Tables

Internally Hash tables use array to store an object, 

Applications of Hash tables
1- spell Checkers
2- Dictionaries
3-  Compilers
4-  Code Editors

We are using Hash Tables with different name
Hash maps in Java
Object in Javascript
Dictionary in python
Dictionary in C#

In JavaScript, there are several ways to implement hash tables 
* Objects: Objects in JavaScript can be used as simple hash tables. However, they have some limitations, such as potential key collisions with built-in properties and the inability to store non-string keys efficiently.
* Maps: The Map object is a more robust implementation of hash tables in JavaScript. It allows any data type as keys and maintains the insertion order.

### Operations:
insert()
lookup()
delete() 

#### Run time complexity:
All have O(1) constant time, because hash function tell us where we should store the  object or lookup in the memory so we don’t have to go through all the items. 

 - - - - - - - - - - - 
