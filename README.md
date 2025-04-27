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
