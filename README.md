# _printf  
![enter image description here](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.gnbclasses.in%2F2023%2F02%2Fexplain-printf-and-scanf-with-example.html&psig=AOvVaw3ICQEKC8ba9n8gQeS2Wkd8&ust=1733072231556000&source=images&cd=vfe&opi=89978449&ved=0CBMQjRxqFwoTCPChsKnDhIoDFQAAAAAdAAAAABAE) 
### What is printf?  

In C language, printf() function is used to print formatted output to the standard output stdout (which is generally the console screen).  The printf function is a part of the C standard library <stdio.h> and it can allow formatting the output in numerous ways
.
### Patterns 


That image shows specifiers that we can use in the printf.  In this case, _printf just allow specifiers like   
|Specifiers|Functions|Description| 
|--|--|--|
|s|print_string|print a string| 
|c|print_char|print just a char| 
|i|print_integer|print a number in base 10|
|d|print_integer|print a number in base 10|
|p|print_pointer|print a memory address in base 16 lowercase| 
|b|print_binary|print a number in base 2|
|x|print_hexadecimal_low|print a number in base 16 lowercase| 
|X|print_hexadecimal_upp|print a number in base 16 uppercase|
|o|print_octal|print a number in base 8| 
|R|print_rot|print a string encoded in rot13 format| 

###Example
![enter image description here](https://www.google.com/url?sa=i&url=https%3A%2F%2Fdev.to%2Femilossola%2Fa-beginners-guide-to-print-integers-in-c-304i&psig=AOvVaw0axN_o7I6wK3r-_a1nOJ_s&ust=1733072463358000&source=images&cd=vfe&opi=89978449&ved=0CBMQjRxqFwoTCID3n53EhIoDFQAAAAAdAAAAABAE)
## Flowcharts

These 3 functions are the bases for this project:

 1. Printf: Is the frontend of all the algorithm, so is the prototype, and just receive the variables
 2. Handler: Is the controller for the string and the formats, and also does the counter for the numbers of bytes that are printing
 3. Percent handler: Compare a list of possible specifiers with the current pattern, and return the corresponding function

![enter image description here](https://i.imgur.com/SjqIUs7.png) ![enter image description here](https://i.imgur.com/ouUh2G4.png)
![enter image description here](https://i.imgur.com/90TRtGH.png)


## Project overview

### Compilation:

All files will be compiled with gcc 4.8.4 using the flags:  -Wall -Werror -Wextra -pedantic

    gcc -Wall -Werror -Wextra -pedantic *.c

### Betty coding style:

All files are written in C and follows the Betty coding style for Holberton School. For more detail, check this page:

[Betty style documentation](https://github.com/holbertonschool/Betty/wiki)

### Authorized functions and macros

* write (man 2 write)
* malloc (man 3 malloc)
* free (man 3 free)
* va_start (man 3 va_start)
* va_end (man 3 va_end)
* va_copy (man 3 va_copy)
* va_arg (man 3 va_arg)
* _putchar(char c)

## Function prototypes

All function prototypes used to compile _printf() are included in the header file **main.h**:
*    int (*get_func(const char *format))(va_list);
*    int _putchar(char c);
*    int _printf(const char *format, ...);
*    int print_str(va_list args);
*    int print_char(va_list args);
*    int print_pct(va_list args);
*    int print_dec(va_list args);

## Function description

**int _printf(const char \*format, ...)**

This function produces output under the control of a *format string* that specifies how subsequent arguments (or arguments accessed via the variable-length argument of stdarg(3)) are converted for output.

The **format string** is composed of zero or more directives:
1. Ordinary characters that are copied unchanged to the output stream. (except %)
2. Conversion specifications, each of which results in fetching zero or more subsequent arguments. Each conversion specification starts with the character %, ends with a conversion specifier ( which is a letter).


## File description

* **_printf.c:** - contains the function _printf()
* **_putchar.c:** - contains the function _putchar()
* **man_3_printf:** - manual page for  _printf() function.
* **get_functions.c** - contains the function get_func()
* **file_functions.c** - contains the functions print_char, print_str and print_pct for the case of printing character, string and '%'
* **file_func_dec_int.c** - contains the function print_dec for the case of printing decimal and integer
* **main.h** - contains all headers, prototypes and structure declaration


## Author
##### Salali Fatima
Holberton School, Cohort 25
##### Abdullayeva Chichak
Holberton School, Cohort 25 
