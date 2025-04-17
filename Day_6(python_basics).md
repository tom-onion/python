# Day 6: Data Structures - Dictionaries

Today, we'll explore **dictionaries**, a powerful and versatile data structure in Python that allows you to store data in key-value pairs. Unlike lists and tuples, which are indexed by numbers, dictionaries are indexed by unique keys.

**Morning:**

1.  **Introduction to Dictionaries:**
    * Dictionaries are unordered collections of key-value pairs. This means the order in which you define the pairs is not necessarily the order in which they are stored or retrieved (though in Python 3.7+, dictionaries remember insertion order).
    * Each key in a dictionary must be unique. Values, however, can be duplicates.
    * Keys are typically immutable data types like strings, numbers, or tuples. Lists cannot be used as keys because they are mutable. Values can be of any data type.
    * Dictionaries are defined by enclosing key-value pairs in curly braces `{}`, with each pair separated by a colon `:` and pairs separated by commas `,`.
    * **Creating Dictionaries:**
        ```python
        empty_dict = {}
        student = {
            "name": "Dhaya",
            "age": 20,
            "major": "Computer Science"
        }
        grades = {
            "Math": 95,
            "Science": 88,
            "English": 92
        }
        mixed_keys = {
            1: "one",
            3.14: "pi",
            ("a", "b"): "tuple_key"
        }
        ```

2.  **Accessing Dictionary Values:**
    * You can access the value associated with a key using square brackets `[]`, similar to accessing elements in a list or tuple, but instead of an index, you use the key.
        ```python
        student = {
            "name": "Dhaya",
            "age": 20,
            "major": "Computer Science"
        }
        print(student["name"])   # Output: Dhaya
        print(student["age"])    # Output: 20
        print(student["major"])  # Output: Computer Science
        ```
    * **Using the `get()` method:** The `get()` method is another way to access values. It's often preferred because it allows you to provide a default value to return if the key does not exist, preventing a `KeyError`.
        ```python
        student = {
            "name": "Dhaya",
            "age": 20,
            "major": "Computer Science"
        }
        print(student.get("name"))       # Output: Dhaya
        print(student.get("city"))       # Output: None (key doesn't exist)
        print(student.get("city", "Unknown")) # Output: Unknown (default value)
        ```

**Afternoon:**

1.  **Dictionary Operations and Methods:**
    * **Adding New Key-Value Pairs:** You can add new pairs to a dictionary by assigning a value to a new key.
        ```python
        student = {
            "name": "Dhaya",
            "age": 20
        }
        student["city"] = "New York"
        print(student)  # Output: {'name': 'Dhaya', 'age': 20, 'city': 'New York'}
        ```
    * **Modifying Existing Values:** You can change the value associated with an existing key by assigning a new value to it.
        ```python
        student = {
            "name": "Dhaya",
            "age": 20
        }
        student["age"] = 21
        print(student)  # Output: {'name': 'Dhaya', 'age': 21}
        ```
    * **Removing Key-Value Pairs:**
        * `del dictionary[key]`: Deletes the key-value pair with the specified key. This will raise a `KeyError` if the key does not exist.
        * `dictionary.pop(key)`: Removes and returns the value associated with the specified key. It can also take an optional second argument as a default value to return if the key is not found.
        * `dictionary.popitem()`: Removes and returns the last inserted key-value pair (in Python 3.7+). In earlier versions, it removes an arbitrary key-value pair.
        * `dictionary.clear()`: Removes all items from the dictionary.
        ```python
        student = {
            "name": "Dhaya",
            "age": 20,
            "major": "Computer Science"
        }
        del student["major"]
        print(student)  # Output: {'name': 'Dhaya', 'age': 20}

        grades = {"Math": 95, "Science": 88, "English": 92}
        english_grade = grades.pop("English")
        print(english_grade) # Output: 92
        print(grades)       # Output: {'Math': 95, 'Science': 88}

        item = grades.popitem()
        print(item)         # Output: ('Science', 88) (order might vary in older Python versions)
        print(grades)       # Output: {'Math': 95}

        student.clear()
        print(student)      # Output: {}
        ```
    * **Common Dictionary Methods:**
        * `keys()`: Returns a view object that displays a list of all the keys in the dictionary.
        * `values()`: Returns a view object that displays a list of all the values in the dictionary.
        * `items()`: Returns a view object that displays a list of all the key-value pairs as tuples.
        * `update(other_dictionary)`: Updates the dictionary with key-value pairs from another dictionary. If a key exists in both dictionaries, the value from the `other_dictionary` overwrites the existing value.
        ```python
        student = {
            "name": "Dhaya",
            "age": 20,
            "major": "Computer Science"
        }
        print(student.keys())   # Output: dict_keys(['name', 'age', 'major'])
        print(student.values()) # Output: dict_values(['Dhaya', 20, 'Computer Science'])
        print(student.items())  # Output: dict_items([('name', 'Dhaya'), ('age', 20), ('major', 'Computer Science')])

        additional_info = {"city": "New York", "gpa": 3.8}
        student.update(additional_info)
        print(student)  # Output: {'name': 'Dhaya', 'age': 20, 'major': 'Computer Science', 'city': 'New York', 'gpa': 3.8}
        ```

2.  **Iterating Through Dictionaries:**
    * You can iterate through the keys, values, or key-value pairs of a dictionary using `for` loops.
        * **Iterating through keys (default):**
            ```python
            grades = {"Math": 95, "Science": 88, "English": 92}
            for subject in grades:
                print(subject)
            # Equivalent to:
            for subject in grades.keys():
                print(subject)
            ```
        * **Iterating through values:**
            ```python
            grades = {"Math": 95, "Science": 88, "English": 92}
            for grade in grades.values():
                print(grade)
            ```
        * **Iterating through key-value pairs:**
            ```python
            grades = {"Math": 95, "Science": 88, "English": 92}
            for subject, grade in grades.items():
                print(f"The grade in {subject} is {grade}")
            ```

**Evening:**

1.  **Practice:**
    * Create several dictionaries representing different entities (e.g., a book with title, author, and ISBN; a car with make, model, and year).
    * Practice accessing, adding, modifying, and removing key-value pairs.
    * Experiment with the different dictionary methods (`get()`, `keys()`, `values()`, `items()`, `update()`, `pop()`, `popitem()`, `clear()`).
    * Write programs that iterate through dictionaries to perform tasks like:
        * Calculating the average of values.
        * Finding the key with the highest value.
        * Creating a new dictionary based on conditions applied to the original dictionary.
2.  **Further Exploration (Optional):**
    * Research dictionary comprehensions, which provide a concise way to create dictionaries based on existing iterables.
    * Consider how you might use dictionaries to represent more complex data structures, like a database record or a configuration file.

**Key Takeaways for Day 6:**

* You understand that dictionaries store data as unordered (in Python < 3.7) or ordered (in Python 3.7+) collections of unique key-value pairs.
* You can create dictionaries and access values using keys (both with square brackets and the `get()` method).
* You are familiar with common dictionary operations for adding, modifying, and removing key-value pairs.
* You know how to iterate through the keys, values, and key-value pairs of a dictionary using `for` loops and the `keys()`, `values()`, and `items()` methods.

**Looking Ahead to [Day 7:](https://github.com/python/Day_7(python_basics).md)**

Tomorrow, we will take a break from learning new data structures and focus on **functions**. Functions are reusable blocks of code that perform specific tasks, making your programs more organized, modular, and easier to maintain. Keep practicing with dictionaries!
