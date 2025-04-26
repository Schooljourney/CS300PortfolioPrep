Vector

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
