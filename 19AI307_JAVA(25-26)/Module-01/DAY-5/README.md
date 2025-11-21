
 # Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to reverse a given string.

## AIM:
To a Java program to reverse a given string.

## ALGORITHM :
1. Start the program and read a string input from the user.
2. Create a StringBuilder object with the input string.
3. Use the reverse() method of StringBuilder to reverse the string.
4. Convert the reversed StringBuilder back to a string.
5. Display the reversed string and stop the program.

## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: Lokesh Rahul V V 
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Prompt user for input
        String str = sc.nextLine();

        String reversed = "";

        // Loop through the string from end to start
        for (int i = str.length() - 1; i >= 0; i--) {
            reversed += str.charAt(i);
        }

        // Display the reversed string
        System.out.println("Reversed string: " + reversed);

        sc.close();
    }
}
```

## OUTPUT:
<img width="765" height="202" alt="image" src="https://github.com/user-attachments/assets/35809a36-8324-48f6-a8b6-23ebe572aa03" />

## RESULT:
The program successfully displays the reversed version of the input string.
