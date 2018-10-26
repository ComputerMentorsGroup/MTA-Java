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
This is what’s known as a Console Application. Let’s break this program down a lot. It looks like a lot of code, but all this program does is display the words "Hello World" in the console that shows up when you run this program. Any Java program will need to have a main method in order for the program to work. The main function will let the compiler know where the program is going to start. Also pay attention to semicolons ```;```. They must be in place to end a line of code.

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

In programming, variables are used to hold values in much the same way as they are used in math. The value of a variable can be a number or an object such as a String of text or something else that you define. Variable can be used for:
* Organizing code
* Storing user input
* Managing the current state of the program (more details later)

In the example above ```String name = "Avery";``` is a variable. To declare it we must give it a type (in this case the type is a String). Then we must give it a name. The variables name will help us distinguish it form other variables. The ```=``` operator is used to asign a value to the variable. In the example the value is ```"Avery"```. Keep in muind that because the variable is expecting a string we MUST wrap or text in quotes. 

## If statments

An If statment is what is known as a conditional. It only runs if the condition that it is looking for is true. we can add an else statment after it to do do a task if the other condition is false.
```Java
if(doorUnlocked == true){
    openDoor();
} else {
    unlockDoor();
}
```

## Loops

A loop is a type of conditional statment that does exactley what it sounds like. It repeats a block of code like song on repeat until the condition its looking for is false. to day we will use the Do loop.
```Java
int x = 0;

do{
    x = x + 1;
    
}while(x < 100);
```
This loop will reapete as long as x is less than 100. The unique thing about do loops is that unlike other conditionals the do loop will run ATLEAST once.

## Methods/Function

A method, also known as a function, is a block of code that preforms a task by combining differnt lins of code. Some methods will require the program to return a value. Others, like the main method at the top, will not return a value.

```Java
public boolean checkAge(int i){
    boolean oldEnough = false;
    if(i > 13){
        oldEnough = true;
    }
    return oldEnough;
}
```
The example code is going to check to see if the data passed to it```int i``` is old enough. If they are old enough it will change the value of the oldEnough boolean to true and return that value to the code that called it.

To call this method you would need write this:
```Java
checkAge(19);
```

The data in the perenthises will be sent to the checkAge() method to see if it is true.

##Exercise
Try creating a MadLib program with the what you have learend on this page. You can use Intellij or repl.it to create it. Below is an example
```Java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        
        System.out.print("Enter a exclamation: ");
        String exclamation = checkForWord();

        System.out.print("Enter a adverb: ");
        String adverb = checkForWord();

        System.out.print("Enter a noun: ");
        String noun = checkForWord();

        System.out.print("Enter a adjective: ");
        String adjective = checkForWord();

        // printf prints outs formatted strings but doesn't add a new line
        System.out.printf("\"%s!\" he said %s as he jumped into his convertible %s and drove off with his %s wife.\n", exclamation, adverb, noun, adjective);
        System.out.println("Thank you for playing!\n");
    }

    private static String checkForWord() {
        Scanner scanner = new Scanner(System.in);
        String word = scanner.nextLine();
        boolean isInvalid;
        do {
            isInvalid = word == null || word.isEmpty();
            if (isInvalid){
                System.out.print("Please input a word: ");
                word = scanner.nextLine();
            }
        }while (isInvalid);

        return word;
    }
}
```
