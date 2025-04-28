Big O analysis
Vector:
Runtime analysisi table
Line/Function          Cost   #Execurion  Total Time
Open File               1        1           1
WHILE(read line)        1        n           n
Parse line              1        n           n
Validate formatting     1        n           n
Create CourseObject     1        n           n
Add to data structure   1        n           n
Total                                       o(n)
Advantages

•	Its simplicity in implementation

•	Ideal for small datasets 

•	Simple data structure

•	Maintains the order of the input
Disadvantages
•	Inefficient for large datasets due to O(n) sorting time.

•	Have to manually sort by alphanumeric order 

Hash Table:
Runtime analysisi table
Line/Function          Cost   #Execurion  Total Time
Open File               1        1           1
Read line               1        n           n
Parse tokens            1        n           n
Validate formatting     1        n           n
Create CourseObject     1        n           n
Insert to Hash Table    1        n           n
Total                                       o(1

Advantages

•	Can offer constant time operations for lookup, insertion, or deletion, regardless of the size or order of the data. 

•	It has the ability to handle any type of key, as long as it has a hash function that can generate a unique and consistent index for it. 

•	It is versatile and can be used in applications such as databases and cache.

Disadvantages

•	Resizing, when a hash table becomes too full it can be computationally expensive ( it can degrade to Big O(n).

•	It does not preserve the order of the data, which means you cannot traverse the table in a sequential or sorted way or find the minimum or maximum element (it is not sorted by default).

•	It can suffer from collisions, which are situations where two different keys have the same index. This can reduce the performance of the operations to O(n) time, where n is the number of elements in the table. 

Binary Search Tree
Line/Function                 Cost   #Execurion         Total Time
Open File                       1        1                1
Read line                       1        n                n
Parse tokens                    1        n                n
Validate formatting             1        n                n
Create Course Object            1        n                b
Insert to Binary search tree    log n    n               nlog n                             n log n

Advantages 
•	Efficient for sorted data, O(n log n) insertion and O(n) traversal (automatically maintains sorted order).

•	Dynamic data by growing or shrinking as needed. This can save space and avoid wasting memory (it saves the memory by only storing what is necessary).

Disadvantages 
•	More complex to implement, worst-case O(n) if tree is unbalanced, which means that some branches of the tree are much longer than others. 

•	It can be inefficient for searching for keys that are not comparable, such as strings or objects. In this case, you might need to define a custom comparison function or use a different data structure.
•	Requires additional logic to keep the tree balance.

Recommendation

Vectors are good for small data sets but not efficient for search or sorting at scale.
Hash Tables provide fast access but lack built in order. Best if frequent look ups are needed but not ideal for sorted outputs without extra steps. Binary search tree is ideal for the natural created order in efficient look up. I would recommend the Binary Search Tree for ABCU final look up. It automatically sorts out our output, its efficient with look up and insertion which is based off performance when compared to Hash Table, Binary Search Tree maintains it automatically and compared to vector it is a lot more efficient. It has clean traversal, which makes it useful for ABCU course application






---
Below is the code that List that sort and print course list in Alphanmeric order

---

void printCourseList(TreeNode* node) {

		if (node != nullptr) {
			printCourseList(node->leftChild);
			cout << node->course.number << ", " << node->course.title << endl;
			printCourseList(node->rightChild);
		}
	}
---


CS 300 Journal
Kimberly Blackwood
SNHU
CS-300 Portfolio
Professor L.Gruner
April 19, 2025


1.What was the problem you were solving in the projects for this course?
The problem that I was solving in the projects for this course were related to implementing and using data structures such as Linked List, Hash Tables and Binary Search. I created a program for auctions using a Linked List and used Hash Table to store and retrieve data to the user. I also implemented Binary Search to do a quick sort on the data.

2.How did you approach the problem? Consider why data structures are important to understand.
I approached the problem by :
•	First identify the problem, this is done by distinctly defining the problem and its desired outcome.
•	Consider the data, the type of data being worked on is thought about and the operations that needs to be performed.  Such as sorting ,search and deleting.
•	Choose the right data structure, select a data structure for the operations and problem that needs to be solved. Hash Table was used for fast look up because it has keys and Linked List was used for insertion and deletion.
•	Develop an algorithm, to solve the problem I design an algorithm that uses the chosen data structure.  After selecting the correct data structure, I selected the appropriate algorithm.
•	Optimize, analyze the complexity of the solutions, and consider ways to improve it.
•	Test and refine, test the solution, and refine it as much as needed based on the results. (Geeks for Geeks, 2024).
It is important to understand data structure because they can offer many benefits to the computer programs, such as improving the efficiency and speed of the algorithms. When the correct data structure is selected for the data and operations it reduces the time and space complexity of the code, making it run faster and use less memory.  Also, the correct data structure  can enhance the readability and maintainability of the code by utilizing clear and consistent structures. This will prevent errors and bugs while making the code easier to understand and modify (Geeks for Geeks, 2024)

3.How did you overcome any roadblocks you encountered while going through the activities or project?
When I encountered roadblocks, while going through the activities or project I did my research on scholarly articles that have information on each topic. I reviewed the zybooks, for example zybooks helped me tremendously on quick sort and selection sort.  It provided well detailed examples. I also contacted the tutors that the school offers us.  The tutors helped me when I encountered roadblocks such as when executing the code , sometimes the error was due to me having too many curly braces. They were able to quickly see that and helped me to correct them.

4.How has your work on this project expanded your approach to designing software and developing programs?
Working  on this project expanded my  approach to designing software and developing program by introducing me to Big O notation. Big O Notation is a way to describe how the time or space needed by an algorithm grows as the size of the input increases. When it is said that a function f(n) is O(g(n)), it means that f(n) will not grow faster than a certain multiple of another function g(n) once the input size is large enough. In other words, f(n) is bounded by g(n) scaled up by some constant value for large inputs (Research Gate, 2022).  In Binary Search I used Big O for look up. It helps me to decide which of the algorithm to use by telling me which one is faster. It measures the execution time of the algorithm. By applying Big O I prioritized the code made it efficient and reduced the execution time.

5.How has your work on this project evolved the way you write programs that are maintainable, readable, and adaptable?
My work on these projects has improved my ability to describe the purpose of codes, techniques implemented to solve problem, challenges encountered, and approaches to overcome the challenges. I now can write pseudocodes with clear step by step logic such as outlining my Binary Search and handling  duplicate values before writing the actual code.
My algorithm specifications functioned in all cases. I was able to make sure that data structure specifications were met completely and functioned in all cases. My code annotations explained and facilitated navigation of the code. Both algorithms and data structures were implemented in such a way that they can be reused in other programs. I was able to make my codes follow proper syntax and demonstrate consistent whitespace to reduce debugging time, and variable naming.

References
Geeks for Geeks.(2024). Top Reasons for Failure in Data Structure and Algorithmshttps://www.geeksforgeeks.org/top-reasons-for-failure-in-data-structures-and-algorithms/
Research Gate.(2022).The Big O of Mathematic and Computer Science.https://www.researchgate.net/publication/357583960_The_Big-O_of_Mathematics_and_Computer_Science
![image](https://github.com/user-attachments/assets/ab873f3e-d497-4915-80c6-66fb8c46e1bd)
