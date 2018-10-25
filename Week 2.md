# Getting Started

Java is a general-purpose computer programming language designed to produce programs that will run on any computer system.
The most basic Java Application will look like this:


```Java
public class Main {
    public static void main(String[] args) { 
      
      System.out.print("Hello World");
  }
}
```
## Details
This is what’s known as a Console Application. Let’s break this program down a lot. It looks like a lot of code, but all this program does is display the words "Hello World" in the console that shows up when you run this program. Any Java program will need to have a main method in order for the program to work. The main function will let the compiler know where the program is going to start.

Print is a function that displays text on the consloe for the user to see.
```Java
// This will just display the text "Hello World" to the user.
System.out.print("Hello World");
```
There are three versions of the print function. The first is simply "print()". This will only print a string to the console. You will need to add "\n" to create a new line after. Alternitevly we can use the function "println()". This version of print will create a new line after it prints to the console.

```Java
// This will just display the text "Hello World" and add a new line under it.
System.out.println("Hello World");
System.out.println("This will appear on a new line!");
```
Another way of using the print function is to use the "printf()" function. This command will print out a line of text but will also use placeholders, so the user/program can add data to the print function and give it a degree of flexibility. 

```Java
String name = "Avery";
System.out.println("Hello %s", name); // This will display change %s to the value of the variable name. So, the text "Hello Avery" should appear in the console.
```

## Variables

In programming, variables are used to hold values. The value of a variable can be a number or an object such as a String of text or something else that you define. Variable can be used for:
* Organizing code
* Storing user input
* Managing the current state of the program (more details later)

### Most Common Types

* int - holds integer values (i.e. whole numbers)
* float - holds floating point values (i.e. decimal values) 4 bytes sized.
* double - holds larger decimal values (twice as large as float)
* boolean - holds either true or false (boolean values)
* char - holds only one character
* string - holds a series of characters (text)
An `=` symbol sets the value of the variable to the value specified on the right-hand side of the symbol. For example:

```Java
int y = 100 / 2; // y will equal 50 because math
string name = "Alex"; // Double quotes for string
char first = 'A'; // Single quotes for char
boolean v = true; // can only be true or false
long x = 2;
long l = x * 2; //will equal 4 because x was set to 2
float f = 3.55555f; // You must put the f in front of the number or the program will assume its a double (causing an error).
double d = 4.9999999; // Double is the default floating type variable so it doesn't need a clarification lice decimal and float.

```
### Variable naming
* Can contain uppercase and lowercase letters, numbers, and underscores.
* CANNOT start with a number or contain spaces
* Names are case sensitive.
* Should start with a lowercase letter but is not mandatory.
    * It is common practice to define variables with lowerCamelCaseNames meaning the first word is lower case and all proceeding words are upperCase
    
```Java
string firstName = "Alex"; // is allowed
string LastName = "Jones"; // is allowed but not a recommended naming standard
string 1stName = "Barbra"; // this name is not allowed
string iAmNumber1 = "Ann"; // this is allowed
```

### Other Types
* double - holds floating point values. 8 bytes sized
* decimal - holds floating point values. 16 bytes sized. Optimal for financial and monetary calculations as it has higher precision.
* byte - holds small integer values from 0 - 255.
* sbyte - signed byte, holds integer values from -128 to 127.
* unit - holds only positive integer values.
* long - Same as an integer but is bigger.
* ulong - unsigned long, same as long but only holds positive values.
* short - holds small integer values from -32,768 to 32,767.
* ushort - unsigned short, same as short but only holds positive numbers
