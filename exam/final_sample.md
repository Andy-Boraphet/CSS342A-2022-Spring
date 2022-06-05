# SAMPLE

## 2022 UWB CSS 342(A) Final Exam (50pt)


**1. (2pt) What's the time complexity of bubble sort and insertion sort, respectively?**
```


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
            std::cout << "I love C++" << std::endl;
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
            data[i] = (i % 5 == 0) ? (i + 1) : (i + 5);
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


```




**5.1 (15pt) What's the pre-order, in-order and post-order traversal of the following binary tree**
```bash
         5
        / \
       4   7
      /     \
     1       9
    /       
   3        
```

```
pre-order: 


in-order:


post-order:
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
    // TODO: add your answer here
}
```

**7. (2pt) what's the difference between std::map and std::unordered_map in terms of search performance?**
```


```

**Extra credit 1 (5pt): (5pt) Given two hashmaps, both defined as:**
```c++
std::unordered_map<int, int>
``` 
Design a code to check whether the two maps contain the exact same data as efficient (fast) as possible. 

Code and/or text description of your design both okay.
```



```

