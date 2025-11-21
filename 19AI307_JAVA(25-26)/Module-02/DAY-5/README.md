# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".
<img width="328" height="133" alt="image" src="https://github.com/user-attachments/assets/233085f7-fc84-417f-866a-8912e9ab32fe" />

## AIM:
To Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".

## ALGORITHM :
1.Start
2.Create a class Calculator.
3.Inside the class:
4.Define a non-static method add(int a, int b) that returns a + b.
5.Define a static method info() that prints "Calculator is ready".
6.In the main() method:
7.Call the static method using the class name.
8.Create an object of Calculator.
9.Call the non-static add() method and print the result.
10.End


## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class Calculator 
{
    static void info()
    {
        System.out.println("Calculator is ready");
    }

    int add(int a, int b)
    {
        return a + b;
    }
}

class prog 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n1, n2;
        n1 = sc.nextInt();
        n2 = sc.nextInt();   
        Calculator c = new Calculator();
        Calculator.info();
        System.out.println("Sum: " + c.add(n1, n2));
    }
}
```

## OUTPUT:
<img width="758" height="301" alt="image" src="https://github.com/user-attachments/assets/d2f557b9-10d3-4844-bbb9-6d6e7e456c37" />

## RESULT:
The program successfully prints the static method message and calculates the sum using the non-static method.
