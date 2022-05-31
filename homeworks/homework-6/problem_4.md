<img width="40%" alt="image" src="https://user-images.githubusercontent.com/252020/171221986-94791b45-a81a-4d0a-a8bb-b262c1d4a4a1.png">

## (50pt) Final Project

Important note here: **This counts as 50% of the final exam points**.

### Storing large amount of data

The story here is that we need to store a large number of user records. Each record contains username, age and a set of hobbies. What's your favorite hobby by the way?

The data entry is model as the following:

```c++
class Record {
private:
    unsigned id;
    std::string name;
    unsigned age;
    std::unordered_set<std::string> hobbies;
...
...
}
```

When a user data is inserted into our data store, a self monotonically increasing *id* is assigned to the record with the user data. For simplicity, the id here matches the array index id. There could be cases where they differ but it's out of the scope for our little example here.

User data is stored in an std::vector as follows:

```c++
    std::vector<Record> table;
```

This vector or "collection" of data altogether is called a table. 

"Why a vector?" you ask? It goes to one of the key benefit of using vector comparing to other data structures we've covered: **Random Access**. 

### Fast Search

The purpose of storing all these data is so we could search them by a certain way. For example, search by name, age or hobbies. And with large amount of records, we want the search to be as fast as possible. As [discussed in lecture](https://youtu.be/fy7bFpptVco?t=388), additional data structures are needed to speed up the search, similar to the index section at the end of a book. It helps you quickly locate where a certain word or phrase appears in the book without having to go through it page by page, which could take hours.

Here's an illustration from the lecture slide:

<img src="https://user-images.githubusercontent.com/252020/171221019-dcfa7a32-46a8-4ef5-bef1-7ee77ac945cd.png" width="40%">

An index is modelled as:

```c++
template<typename KeyType>
class Index {

public:
    virtual void insert_record(KeyType key, unsigned record_id) = 0;

    virtual void find_records(KeyType key, std::vector<unsigned> &found_record_ids) = 0;

    virtual void find_records_by_age_range(KeyType lower_bound,
                                           KeyType upper_bound,
                                           std::vector<unsigned> &found_record_ids) = 0;
};
```

So the input to an idex is a key or a range of keys, and the output is a set of record *id* that matches the given key. Note there could be multiple matches, and therefore the output is stored in a vector. Using the output ids from the index, the corresponding records can be quickly located. Quickly how? Because records are stored in a vector which supports O(1) random access using. 

