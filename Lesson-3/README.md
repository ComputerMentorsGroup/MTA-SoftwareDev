# Lesson 3

Writing your first program:

1. Open Microsoft Visual Studio
2. Create a New Project
3. Choose Windows - Console Application
4. Name the project Input
5. Position the cursor between the { } (curly brackets) of the Main() method and type the code below.
6. Press F5 when completed to see the results.

```C#
Console.Title = "Input";

Console.Write("Please Enter Your Name: ");
string name = Console.ReadLine();

```

## Details

* `Console.Title = "Input";`
    * This names the Console Application "Input"
* `Console.Write("Please Enter Your Name");`
    * Prints the statement between "s to the Console Window
* `string name = Console.ReadLine();`
    * Whatever the user inputs is read by the console as a **string** with the variable **name**
    
    
Now let's add a few lines to this!


    
```C#
Console.Title = "Input";

Console.Write("Please Enter Your Name: ");
string name = Console.ReadLine();

Console.WriteLine("Welcome " + name + "!");
Console.ReadKey();

```
## Details
* `Console.WriteLine("Welcome " + name + "!");`
  * The console will print whatever is stored in the variable **name**
* `Console.ReadKey();`
  * This statement calls upon the ReadKey method of the Console class to wait for any key to be pressed (Press Any Key to Continue)
    https://www.youtube.com/watch?v=st6-DgWeuos
    
# Exercise

A challenge relating to the original sample code should go here.
