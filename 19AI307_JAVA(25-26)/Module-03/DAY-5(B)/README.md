# Ex.No:3(F) WRAPPER CLASS
## QUESTION:
Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.
<img width="416" height="124" alt="Screenshot 2025-11-21 144525" src="https://github.com/user-attachments/assets/5f242592-1efb-46c7-ab3f-86b05a21a4c1" />

## AIM:
To Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.

## ALGORITHM :
1.Start
2.Read a number from the user.
3.Convert the number to a string using Integer.toString(number) to count digits.
4.Store the digit count.
5.Use Math.pow(digit, numberOfDigits) to raise the digit to the power.
6.Add the result to sum.
7.Compare the sum with the original number.
8.If equal → It is an Armstrong number.
9.Else → Not an Armstrong number.
10.End.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ArmstrongCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int originalNum = num;
        int digits = Integer.toString(num).length();
        int sum = 0;
        while (num > 0) {
            int digit = num % 10;
            sum += Math.pow(digit, digits);
            num /= 10;
        }

        if (sum == originalNum) {
            System.out.println(originalNum + " is an Armstrong number.");
        } else {
            System.out.println(originalNum + " is not an Armstrong number.");
        }
    }
}

```
## OUTPUT:
<img width="846" height="200" alt="Screenshot 2025-11-21 144629" src="https://github.com/user-attachments/assets/6a1dd2e1-fc0e-4406-9e7b-40e29e368c4c" />

## RESULT:
The program successfully checks whether the given number is an Armstrong number using Math.pow() and the Integer wrapper class, and displays the correct output.



