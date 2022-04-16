## 2022 UWB CSS 342(A) Quiz-1

### Anaswer In Code
Solution code can be found [here](https://github.com/a-teaching-goose/2022-342-code-along/tree/quiz-1)

Open it in CLion and you can run it.


### Task 1 (5pt)

The following code is *supposed to* return an array of two numbers and then print these numbers out.

```c++
int *foo_ret_stack_ptr(int size) {
    int array[2] = {12, 34};
    return array;
}

int main(int argc, char **argv) {
    int *ptr = foo_ret_stack_ptr(2);
    for (int i = 0; i < 2; i++) {
        std::cout << ptr[i] << "\n";
    }
}
```

Please explain the memory usage problem in this code, and how you would fix it.

**Answer:**
"Dangling pointer". ptr returned from foo_ret_stack_ptr is pointing to invalid address. To fix, use new in the foo_ret_stack_ptr function and return the pointer.

```c++
    int *array = new int[2]{12, 34};
    return array;
```

Also need to delete array in main before finishing. 


### Task 2 (10pt)

Given the following lines:

```c++
int main(int argc, char **argv) {
  int *arr3 = new int[5]{5, 6, 7, 8, 9};
  int *p = &arr3[3];
  *p = 789;
  delete arr3;
}
```

What are all the values in array *arr3* after running this section? (5pt)

**Answer:**
{5, 6, 7, 789, 9}

Does this code have any memory problem? And if yes, how would you fix it? (5pt)

**Answer:**
Yes, to fix, use:
```c++
delete []arr3;
```

### Task 3 (10pt)

Given the following lines

```c++
int b = 10, c = -2;
int &a = b;
int &d = a;
a++;  
c -= 2;
a = c;  // here
d = d + 1;
```

What does the line with the comment "here", also shown below, do? (5pt)
```c++
a = c;
```

**Answer:**
Assign the value of c, which is -4, to variables referenced by a, which is b and d

After running this section, the value of **a** is **-3**. Explain how variable **a** goes from its initial value 10 to -3. (5pt)

**Answer:**
reference a and d both reference variable b;
a++;

```c++
a++;  // a = 11
c -= 2; // c becomes -4, does not affect a at this line
a = c;  // a (b, d) become -4
d = d + 1; // (a,b,d) become -3 (-4+1), because a is a reference (alias) of b, and d is also a reference (alias) of b
```

### Task 4 (5pt)

Given the following Laptop class

```c++
class Laptop {
private:
    std::string brand;
    int model_year;

public:
    Laptop(const std::string &brand, int modelYear) : brand(brand), model_year(modelYear) {}

    void start_up() {
        std::cout << "laptop " + brand + " (" + std::to_string(model_year) + ") is starting up";
    }
};
```

And this function:

```c++
Laptop *borrow_laptop() {
    Laptop *laptop_loaner = new Laptop("Dell", 2021);
    return laptop_loaner;
}
```

Please explain the issue with the following usage and how you would fix it:

```c++
int main(int argc, char **argv) {
    Laptop *my_borrowed_laptop = borrow_laptop();
    my_borrowed_laptop->start_up();
}
```

**Answer:**
add 
```c++
delete my_borrowed_laptop
```
at the end of the main function.

### Task 5 (10pt)

Your classmate Jimmy is complaining the following code "doesn't work". He's trying to write a function to return the larger of two integers. And in the main function he's calling that function for a quick test.

Your time to shine with your C++ knowledge! 

```c++
int max(int &a, int &b) {
    return (a>=b) ? a : b;
}

int main(int argc, char **argv) {
    int x = max(1, 2);
    std::cout << x << std::endl;
}
```

What problem do you see in his code (5pt)? And how would you fix it (5pt)?

**Answer:**
problem: code won't compile because max function is take references as parameters while main is passing in integer values, which are not variables to match the reference parameter in function max.
<img width="1269" alt="image" src="https://user-images.githubusercontent.com/252020/163688646-a3c8715a-72f1-4afd-8dd5-940956f7ef25.png">

To fix, use variables to call max

```c++
    int a = 1, b = 2;
    int x = max(a, b);
    std::cout << x << std::endl;
```
