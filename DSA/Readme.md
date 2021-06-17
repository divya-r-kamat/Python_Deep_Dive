## Python Datastructure and Algorithms

Big(O) notation is a language we use to talk about how long a algorithm takes to run, we can compare two different algorithm or functions using Big(O) to find which one is better than the other with regards to scale, regardless of our machine/computer differences.

We measure Big(O) using below graph, it means when we go bigger and bigger with our input how much does the algorithm or function slow down or the number of operations that we need to do as the inpur increases. This is called algorithmic efficiency, different functions have differnt big-O complexities. The less or lower it slows down the better it is.

<img src="https://user-images.githubusercontent.com/42609155/121635235-8a145380-caa3-11eb-843b-62698516a85c.png" width="500">


- O(n) - This is one of the most common Big-O notation, it indicates that as the number of inputs (n) increase, the number of operations also increases, also called as Linear Time.

- O(1) - This is called Constant time, no matter how many inputs we have the number of operation is just one or constant amount of time.

- O(n2) - Quadratic time, as the number of elements increases the number of operations increases significantly

- O(n!) - adding a loop for every element iterating over

Basic Rules for Big-O :
- Rule1 : We always care about the Worst Case Scenario
- Rule2 : Drop the Constants
- Rule3 : Different terms for inputs, O(m+n) - one for each input
- Rule4 : Drop non dominants


There are two kinds of complexities:
- Space Complexity associated with memory  i.e memory required by the algorithm
- Time complexity associated with cpu (speed) i.e how long it takes the algorithm to run

What causes space complexity?
- variables
- Data Structures
- Function Call
- Allocations

Note: When we talk about space complexity we talk about additional space (memory), we dont include the space taken up by the inputs. We dont really care how big the input is, we only care what happens inside a function, are we adding any additional space?

