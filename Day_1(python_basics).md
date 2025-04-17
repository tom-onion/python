# Day 1: Getting Started with Python

Welcome to your Python journey! Day 1 is all about setting up your environment and understanding the very basics of the language.

**Morning:**

1.  **Install Python:**
    * **Windows:** Go to the official Python website (python.org), download the latest stable version for Windows, and run the installer. **Important:** Make sure to check the box that says "Add Python to PATH" during the installation. This allows you to run Python from the command prompt.
    * **macOS:** Python 3 is usually pre-installed on macOS. You can check the version by opening Terminal (Applications > Utilities > Terminal) and typing `python3 --version` or `python --version`. If it's not installed or you want a newer version, download the installer from python.org.
    * **Linux:** Python is generally pre-installed. Open your terminal and check the version using `python3 --version` or `python --version`. If needed, you can install it using your distribution's package manager (e.g., `sudo apt-get update && sudo apt-get install python3` on Debian/Ubuntu, `sudo yum install python3` on CentOS/Fedora).
2.  **Install a Code Editor (Optional but Recommended):**
    * While you can write Python code in a simple text editor, a dedicated code editor or Integrated Development Environment (IDE) offers features like syntax highlighting, code completion, and debugging tools, which will significantly improve your coding experience. Popular options include:
        * **VS Code:** A free and highly customizable editor with excellent Python support.
        * **PyCharm:** A powerful IDE specifically designed for Python development (has a free Community Edition).
        * **Sublime Text:** A lightweight and fast editor (not free but offers a trial).
        * **Atom:** Another free and customizable editor (development ended, but still usable).
3.  **Your First Python Code:**
    * Open your text editor or IDE.
    * Type the following line of code:
        ```python
        print("Hello, Python!")
        ```
    * Save the file as `hello.py` (the `.py` extension is important for Python files).
4.  **Run Your Code:**
    * **Using the Command Prompt/Terminal:**
        * Open your command prompt (Windows) or terminal (macOS/Linux).
        * Navigate to the directory where you saved `hello.py` using the `cd` command (e.g., `cd Documents/PythonProjects`).
        * Run the script by typing `python hello.py` (or `python3 hello.py` on some systems) and pressing Enter.
        * You should see the output: `Hello, Python!` printed on your console.
    * **Using an IDE:** Most IDEs have a "Run" button or a keyboard shortcut to execute your Python script.

**Afternoon:**

1.  **Understanding the `print()` function:**
    * The `print()` function is a fundamental built-in function in Python used to display output to the console.
    * The text you want to display is enclosed in parentheses and quotation marks (either single `'` or double `"`).
    * Example:
        ```python
        print("This is a string.")
        print('Another string.')
        ```
2.  **Variables:**
    * Variables are used to store data in your program. You can think of them as labels assigned to values.
    * To create a variable, you choose a name and use the assignment operator `=` to assign a value to it.
    * Variable names are case-sensitive (`my_variable` is different from `My_Variable`).
    * Variable names should be descriptive and follow certain rules (e.g., they cannot start with a number, cannot contain spaces, and should avoid using reserved keywords like `print`, `if`, `for`, etc.).
    * Examples:
        ```python
        message = "Hello"
        number = 10
        pi_value = 3.14
        is_python_fun = True
        ```
3.  **Basic Data Types:**
    * Python has several built-in data types. Today, we'll touch upon the most common ones:
        * **String (`str`):** Represents text. Enclosed in single or double quotes. Example: `"Hello"`, `'World'`.
        * **Integer (`int`):** Represents whole numbers (positive, negative, or zero) without a decimal point. Example: `10`, `-5`, `0`.
        * **Float (`float`):** Represents real numbers with a decimal point. Example: `3.14`, `-2.5`, `0.0`.
        * **Boolean (`bool`):** Represents truth values, either `True` or `False`.
    * You can use the `type()` function to check the data type of a variable.
        ```python
        x = 5
        print(type(x))  # Output: <class 'int'>

        y = "Python"
        print(type(y))  # Output: <class 'str'>
        ```

**Evening:**

1.  **Practice:**
    * Try writing a few more `print()` statements with different messages.
    * Declare a few variables of different data types and assign them values.
    * Use the `print()` function to display the values of these variables.
    * Experiment with the `type()` function to see the data type of your variables.
2.  **Further Exploration (Optional):**
    * Look up Python keywords and try to avoid using them as variable names.
    * Read a bit more about the rules for naming variables in Python.
    * If you're using an IDE, explore its basic features like syntax highlighting and running code.

**Key Takeaways for Day 1:**

* You have successfully installed Python on your system.
* You understand the basic structure of a Python program.
* You know how to use the `print()` function to display output.
* You have a basic understanding of variables and common data types (string, integer, float, boolean).

**Looking Ahead to [Day 2:](https://github.com/python/Day_2(python_basics).md)**

Tomorrow, we will delve deeper into data types and learn about basic arithmetic operations in Python. Keep practicing, and don't hesitate to experiment with what you've learned today!