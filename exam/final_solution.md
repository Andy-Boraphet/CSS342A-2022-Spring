## 2022 UWB CSS 342(A) Final Exam (50pt)


**1. (2pt) What's the worst case time complexity of bubble sort and insertion sort, respectively?**
```
O(n^2)

```

**2. (2pt) Explain what "collision" means for the hashtable ("dictionary")?** 
```
multiple key hashed to the same hash key

```

**3. (5pt) Your friend Jimmy (yes, him again) is having trouble with the following code. How to fix all the problems in his code?**

Hint: you can use this [online c++ editor](https://www.onlinegdb.com/online_c++_compiler) to play with the code.

```c++
int& multiple_by_two(int num) {
  num *= 2;  
  return num;
}
int main()
{
    const int size = 10;
    int *data = new int[size];
    for (int i=0; i<size; i++) {
        data[i] = multiple_by_two(i);
    }
    for (int i=0; i<size; i++) {
        cout<< "value is " << data[i] << endl;
    }
}
```

Describe your fix.
```
multiple_by_two return an integer instead of a reference.

add delete []data at the end of main
```

**4. (10pt) Given the following code:**

```c++
#include <iostream>
class BaseClass {
protected:
    int capacity;
    int *data;
public:
    BaseClass() = default;
    BaseClass(int capacity) {
        if (capacity < 1) {
            return;
        }
        data = new int[capacity];
        for (int i = 0; i < capacity; i++) {
            data[i] = i + 2;
            std::cout << "I hate C++" << std::endl; // 4.4 is asking about this line
        }
    }
    virtual int get_capacity() = 0;
    int operator[](int idx) {
        return data[idx];
    }
    ~BaseClass() {}
};
class DerivedClass : public BaseClass {
public:
    DerivedClass(int capacity) {
        this->capacity = capacity;
        data = new int[capacity];
        for (int i = 0; i < capacity; i++) {
            data[i] = (i % 3 == 0) ? (i + 30) : (i + 10);
        }
    }

    int get_capacity() {
        return capacity;
    }
    ~DerivedClass() {
        delete[]data;
    }
};

int main() {
    BaseClass *p_base = new DerivedClass(10);
    for (int i = 0; i < p_base->get_capacity(); i++) {
        std::cout << (*p_base)[i] << std::endl;
    }
    delete p_base;
}
```

**4.1 (2pt) What's the output?**
```
30
11
12
33
14
15
36
17
18
39
```

**4.2 (2pt) In the following line, what does "=0" mean?**
```
    virtual int get_capacity() = 0;
```
```
pure virtual function. this virtual function has no implementation
```

**4.3 (4pt) Running the code as is, valgrind is showing memory leak. How to fix it without changing any member function body (the part between { and })?**
```
==22708== LEAK SUMMARY:
==22708==    definitely lost: 40 bytes in 1 blocks
```

```
make ~BaseClass() virtual

```

**4.4 (2pt) How many times are "I hate C++" printed when running the code? And why?**
```
zero because the base calss constructor is never called.

```


**5.1 (15pt) What's the pre-order, in-order and post-order traversal of the following binary tree**
```bash
         5
        / \
       4   7
      /     \
     1       9
            /
           6
```

```
pre-order: 5 4 1 7 9 6


in-order: 1 4 5 7 6 9


post-order: 1 4 6 9 7 5
```

**5.2 (2pt) Is this tree a BST (binary search tree)? If not, change the value of exactly one node and make it a binary search tree.**
```
not a BST. change 6 to 8
```

**5.3 (5pt) Given the root node of a binary tree, write the code that deletes the tree. This means delete all the nodes in the tree without memory leak. Hint: recursion.**
```c++
template<class T>
class BinaryTree;

template<class T>
class TreeNode {
public:
    friend class BinaryTree<T>;

    T val;
    TreeNode<T> *left;
    TreeNode<T> *right;

public:
    TreeNode() : left(nullptr), right(nullptr) {}

    TreeNode(const T val) : TreeNode() {
        this->val = val;
    }
};

template<typename T>
void delete_tree(TreeNode<T> *tree) {
    if (tree == nullptr) {
        return;
    }

    if (tree->left == nullptr && tree->right == nullptr) {
        delete tree;
        return;
    }

    delete_tree(tree->left);
    delete_tree(tree->right);

    delete tree;
}
```


**5.4 (3pt) Use the tree in 5.1 as input to the delete_tree function, and list the node values in the sequence of visit by delete_tree.**
```
post order: 1 4 6 9 7 5
```


**6. (4pt) Write the function that implements the Fibonacci sequence.**
Fibonacci sequence is a sequence of numbers where each number is the sum of the two preceding ones, starting from 0 and 1.
```
F(0) = 0, F(1) = 1
F(n) = F(n - 1) + F(n - 2), for n > 1.
```
Here are some examples:
```
Input: n = 2
Output: 1
Explanation: F(2) = F(1) + F(0) = 1 + 0 = 1.

Input: n = 4
Output: 3
Explanation: F(4) = F(3) + F(2) = 2 + 1 = 3.
```

**6.1 (2pt) Your code below:**
```c++
int fib(int n) {
    int last_two = 0;
    int last_one = 1;
    
    if (n<=0) {
        return 0;
    } else if (n==1) {
        return 1;
    }
    
    for (int i=1; i<n; i++) {
        int cur = last_two + last_one;
        last_two = last_one;
        last_one = cur;
    }
    
    return last_one;
}
```

**6.2 (2pt) Explain what is "repeated sub-problem" in recursion? and defend that your code for fib(int n) does not have this problem.**
```
function of the same subproblem being called repeated during recursion.

```

**7. (2pt) What's the difference between std::map and std::unordered_map in terms of search performance?**
```
std::map is O(lgn) while std::unordered_map is O(n) in worst case and O(1) in average case

```

**8. (10pt) To store a large number of user record (such as user name, id, hobbies), discuss what would be the best data structure for search and insertion.**

```
use array to store the data, and use a tree structure for fast search 

```

**Extra credit 1 (5pt): (5pt) Given two vectors, both defined as:**
```c++
std::vector<int>
``` 
Design a method to check whether the two vectors contain the exact same data in O(1) time complexity. Note, O(1) is for the checking part of the algorithm. Also, no requirement on space complexity.

Code and/or text description of your design both okay.

Hint: one of the cool tree ADTs we dicussed in lecture.

```
Use merkle tree

```

**Extra credit 2 (5pt): What's the programming language introduced by the guest speaker Rick? And what are some of the key benefits of that language compared to C++?**
```
Rust, memory safety

```

