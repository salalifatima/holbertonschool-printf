# holbertonschool-printf

This repository contains a custom `printf` function as part of the Holberton School curriculum.

## Table of Contents

- [Description](#description)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Files](#files)
- [Testing](#testing)
- [Authors](#authors)

## Description

The project involves creating a custom `printf` function in C, mimicking the standard library's `printf` function. This function supports various format specifiers.

Supported Format specifiers:

- %c is for printing a single character
- %s is for printing a string of characters
- %% is for printing a literal % character
- %d is for printing integer values
- %i is for printing integer values

## Requirements

- GCC (GNU Compiler Collection)
- C standard library

## Installation

Clone the repository:

```
git clone https://github.com/salalifatima/holbertonschool-printf.git
```

Compile the code with your program:

```
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 -Wno-format *.c -o your_program
```

## Usage

Include the header file in your C program:

```
#include "main.h"
```

Use the _printf function similar to the standard printf function:

```
_printf("Hello, %s!\n", "world");
```

Example Code:

```
#include "main.h"

int main(void)
{
    _printf("Character: %c\n", 'H');
    _printf("String: %s\n", "Hello, world!");
    _printf("Integer: %d\n", 42);

     return (0);
}
```

## Files

- README.md: This file.
- _printf.c: The main printf function implementation.
- _putchar.c: Helper function to write a character to stdout.
- main.h: Header file with function prototypes.
- man_3_printf: Man page for _printf() function.
- print_number.c: Functions to handle number printing.
- print_string.c: Functions to handle string printing.

## Testing

To test the _printf function, you can use the provided test cases or write your own. Ensure that your test cases cover various format specifiers and edge cases.

Example Test Code:

```
#include <stdio.h>
#include "main.h"

int main(void)
{
    int len1;   
    int len2;

    len1 = _printf("Character: %c\n", 'H');
    len2 = printf("Character: %c\n", 'H');
   
    printf("Custom printf length: %d\nStandard printf length: %d\n", len1, len2);    

    len1 = _printf("String: %s\n", "Hello, world!");
    len2 = printf("String: %s\n", "Hello, world!");
    
    printf("Custom printf length: %d, Standard printf length: %d\n", len1, len2);

    len1 = _printf("Integer: %d\n", 42);
    len2 = printf("Integer: %d\n", 42);

    printf("Custom printf length: %d, Standard printf length: %d\n", len1, len2);
   
    return (0);
}
```

Compile and run the test code:

```
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 -Wno-format *.c -o test_printf
./test_printf

## Author
##### Fatima Salali
Holberton School, Cohort 25
##### Chichak Abdullayeva
Holberton School, Cohort 25
