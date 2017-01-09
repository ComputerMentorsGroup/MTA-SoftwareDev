# Most Common

* int - holds interger values (i.e. whole numbers)
* float - holds floating point values (i.e. decimal values) 4 bytes sized.
* double - holds larger decimal values (twice as large as float)
* bool - holds either true or false
* char - holds only on character
* string - holds a series of characters (text)
An = symbole means that the varible is the value given as shown below.
```C#
int y = 100 / 2; // y will equal 50 because math
string name = "Alex"; // Double quotes for string
char first = 'A'; // Single quotes for char
bool v = true; // can only be true or false
long l = x * 2;
float f = 3.55555f; // You must pput the f behind the number or the console will give an error saying lookking for a double.
double d = 4.9999999; // Double is the defualt floating type varible so it doesn't need a clarification lice decimal and float.
```
# Variable naming
* Can contain uppercase and lowercase letters, numbers, and underscores.
* CANNOT start with a number or contain spaces
* Names are case sensitive.
* Should start with a lowercase letter but is not mandatory.
```C#
string firstName = "Alex"; // is allowed
string LastName = "Jones"; // is allowed
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

