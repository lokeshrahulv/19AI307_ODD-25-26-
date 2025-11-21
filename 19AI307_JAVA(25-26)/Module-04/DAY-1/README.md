# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
Write a program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.

## AIM:
To write a program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.

## ALGORITHM :
1.Start.

2.Read two integers from the user:

   num1 (dividend)

   num2 (divisor)

3.Check if num2 == 0

   If yes, display: “Error: Division by zero is not allowed.”
   
   If no, perform division → result = num1 / num2

5.Display the result

6.End

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class prog{
    public static void main(String[] args){
        int a,b;
        Scanner sc=new Scanner(System.in);
        try{
            a=sc.nextInt();
            b=sc.nextInt();
            System.out.println("Result: "+a/b);
        }
        catch(Exception e){
            System.out.println("Error: Division by zero");
        }
    }
}
```
## OUTPUT:
<img width="776" height="293" alt="image" src="https://github.com/user-attachments/assets/27409663-ed5d-4162-8bac-7320251e4bb8" />

## RESULT:
The program successfully performs division and safely handles the case when the second number is zero, preventing a runtime error.


