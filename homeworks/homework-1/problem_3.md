## (30pt) Identify The Perfect Customers

The purpose of this homework is to practice **TDD (Test Driven Development)**. 

A company called HoveringCar has a group of social media influecers to promote its products. Based on the followers of each influencer, HoveringCar can identify some potential customers to reach out to for further engagement.

In this work, we are employing a simple algorithm to identify such customers. If a customer has followed all the given influecers, then he/she is chosen as a pential customer if the age is less than or equal to 25. For example, consider the following scenario:

```
Influencer x, followers { {name:a, age: 21}, {name:b, age: 23}, {name:z, age: 26} }
Influencer y, followers { {name:b, age: 23}, {name:c, age: 31}, {name:d, age: 45}, {name:z, age: 26} }
Influencer z, followers { {name:b, age: 23}, {name:z, age: 26} }
```

Then the common follower between influencer x, y and z, hence the potential customer, is {name:b, age: 23}.

The related OOP types are defined [here](), and the function that implements this algorithm is provided [here](). This means you do not need to implement the function, and better yet, you don't even need to look into this function to understand it. 

"What do I do then?" You ask.

In this task, come up with a set of tests for the problem of identifying potential customers based on the description above, without you writing the function code. The tests you write should interrogate the ***find_customer*** function to make sure it follows the algorithm correctly.

Your tests should be written [here in "unit_test_problem_3.cpp"](). 

Note: Your tests should pass upon submission. If you think your test is correct but it fails, please reach out to the instructor immediately for a discussion.
