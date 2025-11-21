# Module 1
# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Write a program to print "Hey, my first java program!" using output statement.

## AIM:
To write a Java program that prints the message "Hey, my first java program!" to the screen.
<img width="341" height="135" alt="image" src="https://github.com/user-attachments/assets/a2afe0c3-32dc-428f-a80d-7025a21bc757" />

## ALGORITHM :
1. Start the program.
2. Define a class named FirstJavaProgram.
3. Inside the class, define the main() method as the program’s entry point.
4. Use the statement System.out.println("Hey, my first java program!"); to display the
 message.
5. Stop the program.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: Lokesh Rahul V V
RegisterNumber: 212222100024
*/
```
## Sourcecode.java:
```
import java.io.*;
public class java
{
    public static void main(String args[])
    {
    System.out.println("Hey, my first java program!");
    }
}
```

## OUTPUT:
<img width="738" height="115" alt="image" src="https://github.com/user-attachments/assets/cf1ef92e-bc4e-4b97-9cfa-b87f82369a0a" />

## RESULT:
To write a Java program that prints the message "Hey, my first java program!" to the
screen.


# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
In a magical building, an elevator behaves oddly:

If the floor number is divisible by 3 and 5, it skips that floor.

If the floor number is divisible by 3 only, it says "Beware!".

If the floor number is divisible by 5 only, it says "Blessings!".

Otherwise, it announces the floor number.

Write a Java program to simulate this elevator logic for a given floor number.
<img width="310" height="127" alt="image" src="https://github.com/user-attachments/assets/cfa02235-685d-472f-842a-fb5de9f061ad" />

## AIM:
 To develop a Java program that checks a given floor number and displays a special
 message based on its divisibility by 3 and/or 5.

## ALGORITHM :
 1. Start the program and read the floor number from the user.
 2. Check if the floor is divisible by both 3 and 5; if true, display "Skipped".
 3. Otherwise, check if the floor is divisible only by 3; if true, display "Beware!".
 4. Otherwise, check if the floor is divisible only by 5; if true, display "Blessings!".
 5. If none of the above conditions are met, display "Floor {floor number}", then stop
 the program.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Lokesh Rahul V V 
RegisterNumber:  212222100024
*/
```
## SOURCE CODE:
```
import java.util.*;
public class java{
    public static void main(String args[]){
        int a;
        Scanner sc=new Scanner(System.in);
        a=sc.nextInt();
        if(a%3==0 && a%5==0)
        {
            System.out.println("Skipped");
        }
        else if(a%3==0)
        {
            System.out.println("Beware!");
        }
        else if(a%5==0)
        {
            System.out.println("Blessings!");
        }
        else
        {
            System.out.println("Floor "+a);
        }
    }
}
```

## OUTPUT:
<img width="588" height="282" alt="image" src="https://github.com/user-attachments/assets/dfbeda97-c306-4ac1-9e7e-042f8a150dd5" />

## RESULT:
The program correctly prints “Skipped,” “Beware!,” “Blessings!,” or “Floor {number}”
according to the elevator's magical rules.


# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to calculate the factorial of a number using a for loop. The factorial of n is the product of all positive integers less than or equal to n.
<img width="435" height="132" alt="image" src="https://github.com/user-attachments/assets/3b9d7085-60f5-448d-b0cf-8dffb6a6dc93" />

## AIM:
To a Java program to calculate the factorial of a number using a for loop. The factorial of n is the product of all positive integers less than or equal to n.

## ALGORITHM :
 1. Start the program and read an integer n from the user.
 2. Initialize a variable factorial to 1 to store the result.
 3. Use a for loop from 1 to n, multiplying factorial by the loop counter in each
 iteration.
 4. After the loop ends, print the value of factorial as the factorial of n.
 5. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Lokesh Rahul V V
RegisterNumber: 212222100024
*/
```
## SOURCE CODE:
```
import java.util.*;

public class Java {
    public static void main(String[] args) {
        int n;
        long fact = 1;
        
        Scanner sc = new Scanner(System.in);
        n = sc.nextInt();
        
        for (int i = n; i >= 1; i--) {
            fact = fact * i;
        }
        
        System.out.println("Factorial of " + n + " is: " + fact);
        
    }
}
```

## OUTPUT:
<img width="847" height="288" alt="image" src="https://github.com/user-attachments/assets/ec613da2-81c7-466a-9784-dcaab5d93007" />

## RESULT:
 The program successfully computes and displays the factorial value of the entered
 number.


 # Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java Program to Find the Average of Array Elements.
<img width="527" height="256" alt="image" src="https://github.com/user-attachments/assets/0b9160b7-e45f-4469-a4e9-3714e521745b" />

## AIM:
To a Java Program to Find the Average of Array Elements.

## ALGORITHM :
1. Start the program and read the number of elements n from the user.
2. Create an array of size n and read n integer elements from the user into the array.
3. Initialize a variable sum to 0 and add all array elements to sum using a loop.
4. Calculate the average by dividing sum by n and store it in a double variable.
5. Display the average value and stop the program.

## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: Lokesh Rahul V V 
RegisterNumber:  212222100024
*/
```
## SOURCE CODE:
```
import java.util.Scanner;
public class AverageOfArray {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        int sum = 0;
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
            sum += arr[i];
        }
        double average = (double) sum / n;
        System.out.printf("The average of elements is %.2f\n", average);
    }
}

```

## OUTPUT:
<img width="887" height="465" alt="image" src="https://github.com/user-attachments/assets/cd7b4993-21a0-4ffd-bcdb-4122bdb08722" />

## RESULT:
 The program successfully computes and displays the average value of all the array
 elements entered by the user.


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




