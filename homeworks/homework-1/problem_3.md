## (30pt) Sum Of Non-uniques

Given an integer array, implement the code that calculates the sum of all *non-unique* elements. The unique elements of an array are the elements that appear **exactly once** in the array.

Example 1:

```
Input: [3]
Output: 0
Explanation: There's only one element and it appears exactly once. So there's no non-unique element.
```

Example 2:

```
Input: [3, 2]
Output: 0
Explanation: There's no non-unique element.
```

Example 3:

```
Input: [2, 3, 2]
Output: 4
Explanation: There's one non-unique element 2, and it appeared twice so 2+2 is 4
```

Example 4:

```
Input: [2, 4, 2, 1, 4, -5, 4]
Output: 13
Explanation: 2 appeared twice and 4 did 3 times. 2 x 2 + 4 x 3 = 16
```



Write the function and as many tests can you can think of to prove your function works correctly. 



### (5pt) Bonus point 

How would you improve your code? Write your answer in a comment section.

"Improve for what?", you ask.

Well, there are many aspects code can be usually improved. To name a few. Say performance, or running time. How many loops do you have? Usually the more loops, the slower you code runs. So can it be reduced? 

How many times does your code visit the entire input array? Sure it depends on inputs. What about the worst case? In this case can it be reduced?

To see the time complexity, add the following test to your problem 3 test

```java
    @Test
    public void largeArrayTest() {
        final int largeNumber = 500000;
        int[] input = new int[largeNumber];
        for (int i = 0; i < input.length; i++) {
            input[i] = i - largeNumber / 2;
        }

        int expect = 0;
        long startTime = System.nanoTime();

        long actual = Problem3.SumOfNonUnique(input);

        long endTime = System.nanoTime();
        long durationInNano = endTime - startTime;

        assertEquals(expect, actual);

        System.out.printf("time: %f seconds", (double) durationInNano / 1e9);
    }
 ```
 
 How many seconds did it take to finish? Can it be reduced?
 

Another possible improvement is code clarity. Is it hard to read? Maybe a better variable name? Some ideas? Sure. [Here](https://a-nickels-worth.blogspot.com/2016/04/a-guide-to-naming-variables.html) is a start.

What about maintainability? Say if you were to add one more test case, how many lines of code do you have to change? Can it be reduced? Try to make it so that one only needs to change two lines to add a new test case.

