<img src="https://user-images.githubusercontent.com/252020/169448091-798c207a-ee2e-44e7-a42a-9b33552fbcb1.png"
     alt="hand"
     width="40%" />

## (25pt) Reverse A Stack

Can't remember the last time I hit gym, but if you have a stack of weight plates, how do you "flip" or "reverse" them? Suppose they are too heavy to be lifted as a whole, so we have to do it plate by plate.

Like this:

<img src="https://user-images.githubusercontent.com/252020/169448681-0d76f78c-a9e7-4c9b-a30c-396c90968f42.png" width="30%">

If we have a stack of data in a Stack ADT, how would you reverse its elements without using any loop or any additional buffer?

This task is to write a function that reverses the values in a Stack ADT using recursion

```java
template<typename T>
void reverse_stack_recursively(Stack<T> &stack) {
    /*
     * TODO: homework
     */
}
```

For example:

* input stack: (top on the left, bottom on the right): [], after the reversal: []
* input stack: (top on the left, bottom on the right): [0], after the reversal: [0]
* input stack: (top on the left, bottom on the right): [0, 1], after the reversal: [1, 0]
* input stack: (top on the left, bottom on the right): [0, 1, 2], after the reversal: [2, 1, 0]
* input stack: (top on the left, bottom on the right): [0, 2, 2, 3], after the reversal: [3, 2, 2, 0]


Requirements:

- No loop of any kind (such as "for", "while") is allowed. Zero point if any loop is used. OK to add helper function.
- Cannot use additional buffer such as array, stack, queue, map. If you want to use something but not sure, please ask.
- Must use recursion.
- Cannot use the push(), peek() and pop() function from the Stack class.

