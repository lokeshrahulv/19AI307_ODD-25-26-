
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


