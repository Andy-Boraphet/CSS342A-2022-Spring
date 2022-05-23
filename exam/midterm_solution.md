## 2022 UWB CSS 342(A) Midterm Exam (100pt)

### "Single Choices"

**1. (2pt) Queues**

- (A) are a "first in, first out" data structure
- (B) are a random access data structure
- (C) are a fixed size data structure
- (D) cannot be implemented using linked lists
A

**2. (2pt) Stacks**

- (A) can be implemented using an array
- (B) are mostly used for problems that require random-access of elements
- (C) cannot be implemented using a linked list
- (D) none of the above
A

**3. (2pt) When overloading a method in a class,**

- (A) the method has to have a unique name
- (B) the method signature must differ from an existing method
- (C) the method name must be preceded by an "o"
- (D) the method signature must be the same as an existing method
D


**4. (4pt)**
In your new company, you are in charge of improving an legacy (old) piece of code that is used to store user record. It's currently using an array, and there's been some complaints from users that adding and deleting data records (stored in the array) are getting very slow. Analyze the problem and propose your solution with reasons.
```
Array is fast for search but slow for inserting and deletion. 
LinkedList is the opposite.
Use Array to store a few Linked Lists. O(lgn) for search in buckets and O(m) for searching/inserting/removing record.
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
    *(p1++) = *(p2 - 1) * 2;

    for (int i = 0; i < 10; i++) {
        std::cout << array[i] << std::endl;
    }
```
(6pt) What's the cout output of the above code ?
```
TBD
```

(4pt) This code has a memory leak. Add ONE statement (not multiple statement on the same line) of code at the very end that
- fixes the memory leak, and 
- **only** using **p2**
```
delete [] (p2-9);

```
With this line of fix, there will be no more memory leak. Using of any variable other than **p2** is not allowed.


**6. (5pt) What's the issue with the following code?**
```c++
// add(int) increments the parameter by 1
int* add(int value) {
  value = value + 1;
  return &value;
}
```
```
dangling pointer

mem address not valid once function returns
```


**7. (10pt) In the following code**
Your classmate Jimmy is again complaining the following code "doesn't work". He's trying to write a function that returns the sum of all values in an object of type class Array, but it's returning wrong values. 

```c++
class Array{
  int* data;
public:
  int size;
  Array(int size) : size(size) {
          data = new int[size];
  }
  int &operator[](int i) { return data[i]; }
  ~Array() { delete data; }
};

int arraySum(Array array) {
    int sum = 0;
    for (int i=0; i<array.size;i++) {
        sum += array[i];
    }
    return sum;
}
```

Function arraySum(Array array) is supposed to return the sum of all values in an object of type class Array but it's returning wrong values. 

You are not very fond of the expression of "doesn't work" but you agreed to help.

How you would fix it? Write down the code for the fix (5pt).
```
missing a copy constructor in class Array. 

Need to verify copy constructor. TBD: validate the default copy constructor.

```

hint: any problem with memory too? (5pt)
```
delete []data;
```

**8. (5pt) What is the output of the following program?**
```c++
#include <iostream>
template<typename T>
T Max(T a, T b) {
   return a < b ? b : a;
}

int main () {
   int i = 12;
   int j = 30;
   std::cout << "Max(i, j): " << Max(i, j) << std::endl;

   float f1 = 2.5;
   float f2 = -20.7;
   std::cout << "Max(f1, f2): " << Max(f1+f2, f1-f2) << std::endl;
}
```
```
TBD: list print out result

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
```c++
template<typename T>
class ComplexNumber {
    T x;
    T y;
public:
    ComplexNumber(T x, T y) : x(x), y(y) {}
    T distance() { return sqrt(x*x + y*y);}
};

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
    int nth_to_last(int);
};
```

Implement the nth_to_last(n) member function that returns the value of the ith node from the end of a linked list.

For example, for a linked list 1->2->3->4->5->N
```
when n is 0, nth_to_last returns 5
when n is 1, nth_to_last returns 4
when n is 2, nth_to_last returns 3
When n is 8, what should nth_to_last do?
```
Note that input list is not always sorted. 

(10pt) Implement the nth_to_last function. **5pt extra credit** if your code only travels through the linkedlist no more than one time.
```c++
int SingleLinkedList::nth_to_last(int n) {




}
```

(5pt) Discuss how you would handle edge cases, for example, when list has only 3 nodes but n is 8. 
```



```


**11. (5pt) What's a unit test? If we ourselves write both function code and test, and the test we write will pass at last, what's the point of having any test?**
```



```

**12. (5pt) Why is it not a good idea to use any kind of printing for software testing?**
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
        steps += 100;
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

**13.1 (5pt) What's the outpout of the following code?** 

```c++
RubberDuck duck("Tim");
int steps = 10;
std::string msg = duck.walk(steps);
std::cout << "duck walk returns '" << msg << "'\n"; 
std::cout << "duck " + duck.get_name() + " walked " + std::to_string(steps) + " steps\n";
```

Here's part of the output
```
duck Tim walked 110 steps
```

Explain why its 110 steps instead of 10 steps printed.
```



```

**13.2 (5pt) What's the outpout of the following code?*** 
```c++
auto *duck = new RubberDuck("Jerry");
std::string &duck_name = duck->get_name();
std::cout << "Duck's name is " << duck_name << "\n";
delete duck;
std::cout << "Duck's name is " << duck_name << " after delete\n";
```
And any problem (hint: memory related) with this code?
```


```

**14. (15pt) Given the following color class**
```c++
#define RED 0
#define GREEN 1
#define BLUE 2
#define YELLOW 3
#define MAGENTA 4
#define CYAN 5
#define WHITE 6

class Color {
public:

    // constructor
    Color(int color);

    // equality
    bool operator==(const Color &rhs) const {
        return color == rhs.color; 
    }

    // exam: add your code here

private:
    int color;
};
```

(10pt) Add to the Color class with a function that allows adding basic color (RED, GREEN, BLUE) together using "+"

```c++
TBD

```

Upon finish, the following test should pass:
```c++
TEST(color, simple) {
    Color red(RED);
    Color blue(BLUE);
    Color green(GREEN);
    Color cyan(CYAN);
    Color yellow(YELLOW);
    Color magenta(MAGENTA);

    ASSERT_EQ(yellow, red + green);
    ASSERT_EQ(magenta, RED + BLUE);
    ASSERT_EQ(cyan, blue + green);
}
```

(5pt) Write down how you would test your function as thorough as possible. You can write code or text description or both for your test plan.
```


```

**15. (5pt) Explain why it's a good idea to declare base class destructor as "virtual"**
```



```
