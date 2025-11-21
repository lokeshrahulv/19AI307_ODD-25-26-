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

