# Day 5: Data Structures - Lists and Tuples

Today, we'll dive into two fundamental data structures in Python: **lists** and **tuples**. These structures allow you to store and organize collections of items.

**Morning:**

1.  **Lists:**
    * Lists are ordered sequences of items. They are **mutable**, meaning you can change their contents after they are created (add, remove, or modify elements).
    * Lists are defined by enclosing items in square brackets `[]`, with items separated by commas.
    * Lists can contain items of different data types.
    * **Creating Lists:**
        ```python
        empty_list = []
        numbers = [1, 2, 3, 4, 5]
        fruits = ["apple", "banana", "cherry"]
        mixed_list = [1, "hello", 3.14, True]
        nested_list = [1, [2, 3], 4]
        ```
    * **Accessing List Elements (Indexing):** Similar to strings, you can access individual elements in a list using their index (starting from 0). Negative indexing can be used to access elements from the end of the list.
        ```python
        fruits = ["apple", "banana", "cherry"]
        print(fruits[0])    # Output: apple
        print(fruits[1])    # Output: banana
        print(fruits[-1])   # Output: cherry (last element)
        print(fruits[-2])   # Output: banana (second to last element)
        ```
    * **List Slicing:** You can extract a portion of a list using slicing, similar to strings.
        ```python
        numbers = [10, 20, 30, 40, 50]
        print(numbers[1:4])  # Output: [20, 30, 40]
        print(numbers[:3])   # Output: [10, 20, 30]
        print(numbers[2:])   # Output: [30, 40, 50]
        print(numbers[:])    # Output: [10, 20, 30, 40, 50] (creates a copy)
        ```

**Afternoon:**

1.  **List Operations and Methods:**
    * **Concatenation:** You can combine two lists using the `+` operator.
        ```python
        list1 = [1, 2, 3]
        list2 = [4, 5, 6]
        combined_list = list1 + list2
        print(combined_list)  # Output: [1, 2, 3, 4, 5, 6]
        ```
    * **Repetition:** You can repeat a list using the `*` operator.
        ```python
        zeros = [0] * 5
        print(zeros)        # Output: [0, 0, 0, 0, 0]
        ```
    * **Common List Methods:** Lists have several built-in methods to modify and manipulate them:
        * `append(item)`: Adds an `item` to the end of the list.
        * `insert(index, item)`: Inserts an `item` at a specific `index`.
        * `remove(item)`: Removes the first occurrence of a specified `item`.
        * `pop(index)`: Removes and returns the item at a given `index`. If no `index` is provided, it removes and returns the last item.
        * `index(item)`: Returns the index of the first occurrence of a specified `item`.
        * `count(item)`: Returns the number of times a specified `item` appears in the list.
        * `sort()`: Sorts the list in place (modifies the original list). You can use `reverse=True` for descending order.
        * `reverse()`: Reverses the elements of the list in place.
        * `clear()`: Removes all elements from the list.
        ```python
        fruits = ["apple", "banana", "cherry"]
        fruits.append("orange")
        print(fruits)       # Output: ['apple', 'banana', 'cherry', 'orange']

        fruits.insert(1, "grape")
        print(fruits)       # Output: ['apple', 'grape', 'banana', 'cherry', 'orange']

        fruits.remove("banana")
        print(fruits)       # Output: ['apple', 'grape', 'cherry', 'orange']

        popped_item = fruits.pop(1)
        print(popped_item)  # Output: grape
        print(fruits)       # Output: ['apple', 'cherry', 'orange']

        index_of_cherry = fruits.index("cherry")
        print(index_of_cherry) # Output: 1

        numbers = [1, 2, 2, 3, 2, 4]
        count_of_2 = numbers.count(2)
        print(count_of_2)   # Output: 3

        numbers.sort()
        print(numbers)      # Output: [1, 2, 2, 2, 3, 4]

        numbers.reverse()
        print(numbers)      # Output: [4, 3, 2, 2, 2, 1]

        fruits.clear()
        print(fruits)       # Output: []
        ```

2.  **Tuples:**
    * Tuples are also ordered sequences of items, similar to lists. However, they are **immutable**, meaning you cannot change their contents after they are created (you cannot add, remove, or modify elements).
    * Tuples are defined by enclosing items in parentheses `()`, with items separated by commas. Although the parentheses are optional in some cases (e.g., when creating a tuple with one or more items), it's generally good practice to include them for clarity.
    * Tuples can also contain items of different data types.
    * **Creating Tuples:**
        ```python
        empty_tuple = ()
        numbers_tuple = (1, 2, 3, 4, 5)
        fruits_tuple = ("apple", "banana", "cherry")
        mixed_tuple = (1, "hello", 3.14, True)
        single_item_tuple = ("apple",)  # Note the trailing comma for a single-item tuple
        not_a_tuple = ("apple")        # This is just a string in parentheses
        ```
    * **Accessing Tuple Elements (Indexing and Slicing):** You can access elements in a tuple using indexing and slicing, just like lists.
        ```python
        fruits_tuple = ("apple", "banana", "cherry")
        print(fruits_tuple[0])    # Output: apple
        print(fruits_tuple[1:3])  # Output: ('banana', 'cherry')
        ```

3.  **Tuple Operations and Methods:**
    * Tuples support concatenation (`+`) and repetition (`*`) operations, similar to lists.
    * Tuples have fewer built-in methods compared to lists due to their immutability. The common methods are:
        * `count(item)`: Returns the number of times a specified `item` appears in the tuple.
        * `index(item)`: Returns the index of the first occurrence of a specified `item`.

**Evening:**

1.  **Practice:**
    * Create various lists and tuples with different data types and nested structures.
    * Practice accessing elements using indexing and slicing.
    * Experiment with the different list methods to add, remove, modify, and search for elements. Observe how these methods change the original list.
    * Try to modify a tuple after it's created. You should encounter an error, reinforcing the concept of immutability.
    * Write small programs that use lists and tuples to store and process data. For example:
        * Store a list of student names.
        * Store the coordinates of a point as a tuple.
        * Iterate through a list and perform some operation on each element.
2.  **Further Exploration (Optional):**
    * Research the performance differences between lists and tuples. When might you choose one over the other?
    * Explore the concept of "unpacking" sequences (lists and tuples) into individual variables. For example: `x, y, z = [1, 2, 3]`.

**Key Takeaways for Day 5:**

* You understand the concept of ordered sequences and the difference between mutable (lists) and immutable (tuples) data structures.
* You can create and access elements in lists and tuples using indexing and slicing.
* You are familiar with common list methods for modifying and querying lists.
* You know the basic operations (concatenation, repetition) supported by both lists and tuples.
* You understand the implications of immutability for tuples.

**Looking Ahead to [Day 6:](https://github.com/tom-onion/python/blob/main/Day_2(python_basics).md)**

Tomorrow, we will explore another important data structure: **dictionaries**. Dictionaries allow you to store data in key-value pairs, providing a more flexible way to organize and retrieve information based on meaningful keys. Keep practicing with lists and tuples!
