## 2022 UWB CSS 342(A) Midterm Exam (100pt) (EXAMPLE)

### "Single Choices"

**1. (2pt) Queues**

- (A) are a random access data structure
- (B) are a "first in, first out" data structure
- (C) are a fixed size data structure
- (D) cannot be implemented using linked lists

**3. (2pt) When overloading a method in a class,**

- (A) the method has to have a unique name
- (B) the method name must be preceded by an "o"
- (C) the method signature must be the same as an existing method
- (D) the method signature must differ from an existing method


**4. (4pt)**
In your new company, you are in charge of improving an legacy (old) piece of code that is used to store user record. It's currently using an array, and there's been some complaints from user that updating data records (stored in the array) is getting very slow. Analyze the problem and propose your solution
```



```

**5. (10pt) Given the following lines**


```c++
    int *array = new int[10];

    for (int i = 0; i < 10; i++) {
        array[i] = (i % 2) ? (i + 1) : (i - 1);
    }

    int *p1 = &array[5];
    int *&p2 = p1;

    p2 += 3;
    *p1 = *(p2 - 1) * 2;

    for (int i = 0; i < 10; i++) {
        std::cout << array[i] << std::endl;
    }
```
(6pt) What's the cout output of the above code ?
```


```


**6. (5pt) What's the issue with the following code?**
```c++
// add(int) increments the parameter by 1
int* add(int value) {
  value = value + 1;
  return &value;
}
```
```



```


**9. (5pt) Convert the folowing class to a template class so it takes a type T instead of float.**
```c++
#include "math.h


class ComplexNumber {
    float x;
    float y;
public:
    ComplexNumber(float x, float y) : x(x), y(y) {}
    float distance() { return sqrt(x*x + y*y);}
};
```
```



```

**10. (15pt) Given the following code:**
```c++
class ListNode {
    friend class SingleLinkedList;
private:
    int val;
    ListNode *next;
public:
    ListNode() : next(nullptr) {}
    ListNode(int val) : val(val), next(nullptr) {}
};

class SingleLinkedList {
private:
    ListNode *head;
public:
    SingleLinkedList() {
        head = new ListNode();
    }
    ~SingleLinkedList();
    int mid_node();
    int fifth_to_last(int);
};
```

Implement the fifth_to_last(n) member function that returns the value of the 5th node from the end of a linked list.

For example, for a linked list 2->9->1->4->5->6->N, it should return 9 becasue 9 is the 5th element from the end of the list.

Another example, for a linked list 7->2->9->1->5->6->N, it should return 2 becasue 2 is the 5th element from the end of the list.


Note that input list is **NOT** always sorted. 

(10pt) Implement the fifth_to_last function. *5pt extra credit* if your code only travels through the linkedlist no more than one time.

```c++
int SingleLinkedList::fifth_to_last(int n) {




}
```


**11. (5pt) What's a unit test? If we ourselves write both function code and test, and the test we write will pass at last, what's the point of having any test?**
```



```


**13. (10pt) Given the following class for rubber duck**
```
class RubberDuck {
public:
    void talk(const std::string &words);

    std::string walk(int &steps) {
        std::string msg;
        for (int i = 0; i < steps; i++) {
        msg += "walk(step " + std::to_string(i) + ")!\n";
        }
        steps += 50;
        return msg;
    }

    RubberDuck(const std::string &name) : name(name) {}

    std::string &get_name() {
        return name;
    };

private:
    std::string name;
};

```

**13.1 (5pt) Number of steps walked**

```c++
RubberDuck duck("Tim");
int steps = 10;
std::string msg = duck.walk(steps);
std::cout << "duck walk returns '" << msg << "'\n"; 
std::cout << "duck " + duck.get_name() + " walked " + std::to_string(steps) + " steps\n";
```

Here's part of the output

```
duck Tim walked 60 steps
```

Explain why its 60 steps instead of 10 steps printed.
```



```
