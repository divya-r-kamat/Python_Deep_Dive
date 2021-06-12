## Variables and Memory References

We can think of memory as a series of slots or boxes that exists in our computer and we can store or retrive data from those slots.When we store data in memory address we may actually use more than one slot at a time, that is called heap. Storing and retrieving the objects from the heap is taken care by python memory manager.

When we write a line a of code, say x=10 and execute this line of code the first thing python does is to creates a object in memory at some address (lets say x1010) and stores a value of 10. x is simply a name for the memory address where the object is stored. So, x is said to be a reference to the object at address x1010. In real terms, x will be equal to x1010 i.e memory address where the value 10 is stored, basically x is a reference to the object at that memory location. 

- Variables in python are always references to objects in memory. 
- We can find the memory address referenced by a variable using the id() function. This function returns a base-10 number, this could be converted to hexadecimal using hex() function if required.


Python memory manager maintains Reference counting for every object in the memory.

We can keep track of objects that are created in the memory, by keeping track of their memory address and how many variables are pointing to the same object. If we say y = x , we are not taking the value of 10 and assigning to y rather the memory reference of x is assigned to y, so y would also point to the same memory address x1010 i.e we are actually sharing the reference and the reference count for x1010 would be 2. Where the variables are deteled python memory manager deletes the objects and the space can be reused.

Reference count of a variable in python can be found using following ways

    sys.getrefcount(variable)
    
The problem with this is passing a variable to getrefcount() creates an extra reference to the same object.

    ctypes.c_long.from_address(address).value

In this case, we just pass the memory address (an integer), not a reference so it doesnot affect reference count


### Garbage Collector

Garbage collector helps identify the circular references and clean them up. 

What is circular reference? Lets say we have a variable x which points to object A and lets suppose the object A has a var y and it references to another object B and this object B also has a instance variable z which points back to object A. Now this is called a circular reference, deleting the variable x will not clean up the objects with circular references by the reference count, this causes memory leak. This is where Garbarge collector comes in.
- GC can be controlled programmatically using the gc module, by default it is turned on
- runs periodically on its own
- can be called manually, and even do own cleanup


### Dynamic Vs Static type

Languages like C++, Java are statically type languages, i.e the datatype is associated with the variable name, whereas Python is dynamically typed, type is not attached to the variable. Built in type() function can be used to determine the type of object currently referenced by the variable


### Object Mutability

Lets say we have a variable var and this references some object in the memory at some memory address say x1000 and lets say the data type of this object is bank_account and this has two instance properties account number and balance. Now suppose, we modified the balance, the internal state changes but the memory address doesnot change. Changing the data inside the object is called modifying the internal state of the object.

An object is said to be mutated, when the internal state (data) of an object is changed and the memory address has not changed, i.e an object whose internal state can be changed is called mutable. But the object whose internal state cannot be changed is called immutable.


Immutable Objects
- Numbers (int, float, booleans etc)
- Strings
- Tuples (tuple is immutable but it can contain mutable elements like lists)
- frozen sets
- user defined class

Mutable Objects
- lists
- sets
- dictionaries
- user defined class





