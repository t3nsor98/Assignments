### Q1)What do you mean by data types? How data type are different from variables?

In C language, data types refer to the kinds of values that can be stored and manipulated in a program. They define the type of data a variable can hold. 

For example, some common data types in C include:

1. **int**: Used for storing integer numbers like -1, 0, 1, 100, etc.
2. **float**: Used for storing floating-point numbers like 3.14, -0.001, etc.
3. **char**: Used for storing single characters like 'a', 'b', '1', '$', etc.
4. **double**: Similar to float, but with higher precision for floating-point numbers.
5. **bool**: Used for storing Boolean values, which can be either true or false.

Variables, on the other hand, are names given to memory locations where data can be stored. They are like containers that hold data. When you declare a variable, you specify its data type, which tells the compiler what kind of data the variable will hold.

Here's an example to illustrate the difference:

```c
#include <stdio.h>

int main() {
    // Declaring variables
    int age; // 'age' is a variable of type int (integer)
    float weight; // 'weight' is a variable of type float (floating-point number)
    char grade; // 'grade' is a variable of type char (character)

    // Assigning values to variables
    age = 25;
    weight = 65.5;
    grade = 'A';

    // Printing values of variables
    printf("Age: %d\n", age);
    printf("Weight: %.2f\n", weight); // %.2f is used to print float with 2 decimal places
    printf("Grade: %c\n", grade);

    return 0;
}
```

In this example, `int`, `float`, and `char` are data types, while `age`, `weight`, and `grade` are variables. The data type specifies the kind of data that each variable can hold.






### Q2)How C language manage input and output in program?

C language manages input and output (I/O) using standard library functions from the `<stdio.h>` header file. Here's a breakdown of the common methods:

**1. Formatted Input:**

- **`scanf` function:** This function is used to read formatted data from standard input (usually the keyboard) and store it in variables. It takes a format string and a list of memory addresses where the read values should be stored.

C

```
int age;
float pi;

printf("Enter your age: ");
scanf("%d", &age);  // Reads an integer and stores in 'age'

printf("Enter the value of pi: ");
scanf("%f", &pi);  // Reads a float and stores in 'pi'
```

**2. Formatted Output:**

- **`printf` function:** This function is used to print formatted data to standard output (usually the console). It takes a format string and optionally a list of variables whose values you want to print.

C

```
int num = 10;
char letter = 'A';

printf("The number is %d and the letter is %c\n", num, letter);
// Output: The number is 10 and the letter is A
```

**3. Unformatted Input:**

- **`getchar` function:** This function reads a single character from standard input and returns its ASCII value as an integer.

C

```
char ch = getchar();
printf("You entered the character: %c\n", ch);
```

**4. Unformatted Output:**

- **`putchar` function:** This function writes a single character to standard output.

C

```
char ch = 'B';
putchar(ch);  // Prints character 'B' to console
```

**5. File I/O:**

C also provides functions for reading from and writing to files, but these are more advanced concepts. They involve opening, closing, and manipulating file pointers.

**Key Points:**

- The `&` symbol (address-of operator) is used to pass the memory address of a variable to `scanf` for storing the input value.
- Format specifiers in `printf` control how the data is displayed (e.g., %d for integers, %f for floats, %c for characters).
- Unformatted I/O functions are less common but can be used for simple character input/output.

By understanding these concepts, you can effectively manage user input and program output in your C programs.