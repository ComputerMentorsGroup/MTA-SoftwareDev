# Variables

In programming, variables are used to hold values. 
The value of a variable can be a number or an object such as a String of text or something else that you define.
Variable can be used for:
* Organizing code
* Storing user input
* Managing the current state of the program (more details later)

# Most Common Types

* int - holds interger values (i.e. whole numbers)
* float - holds floating point values (i.e. decimal values) 4 bytes sized.
* double - holds larger decimal values (twice as large as float)
* bool - holds either true or false
* char - holds only on character
* string - holds a series of characters (text)
An `=` symbol sets the value of the variable to the value specified on the right hand side of the symbol. For example:
```C#
int y = 100 / 2; // y will equal 50 because math
string name = "Alex"; // Double quotes for string
char first = 'A'; // Single quotes for char
bool v = true; // can only be true or false
long x = 2;
long l = x * 2; //will equal 4 because x was set to 2
float f = 3.55555f; // You must put the f in front of the number or the program will assume its a double (causing an error).
double d = 4.9999999; // Double is the defualt floating type varible so it doesn't need a clarification lice decimal and float.
```
# Variable naming
* Can contain uppercase and lowercase letters, numbers, and underscores.
* CANNOT start with a number or contain spaces
* Names are case sensitive.
* Should start with a lowercase letter but is not mandatory.
    * It is common practice to define variables with lowerCamelCaseNames meaning the first word is lower case and all proceeding 
words are upperCase
```C#
string firstName = "Alex"; // is allowed
string LastName = "Jones"; // is allowed but not a recommended naming standard
string 1stName = "Barbra"; // this name is not allowed
string iAmNumber1 = "Ann"; // this is allowed
```

# Other Types
* double - holds floating point values. 8 bytes sized
* decimal - holds floating point values. 16 bytes sized. Optimal for financial and monateray calculations as it has higher precision.
* byte - holds small interger values from 0 - 255.
* sbyte - signed byte, holds interger values from -128 to 127.
* unit - holds only positive interger values.
* long - Same as an interger but is bigger.
* ulong - unsigned long, same as long but only holds positive values.
* short - holds small interger values from -32,768 to 32,767.
* ushort - unsigned short, same as short but only holds positive numbers

