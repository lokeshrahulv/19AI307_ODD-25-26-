# Ex.No:2(B) METHODS

## QUESTION:
Write a method int square(int number) that returns the square of a given number.

## AIM:
To Write a method int square(int number) that returns the square of a given number.

## ALGORITHM :
1.Start

2.Define a method square(int number).

3.Inside the method, calculate number * number.

4.Return the result.

5.Call the method with a sample number (e.g., 5).

6.Print the returned value.

7.End

## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.util.*;
public class prog{
    static int square(int number){
        return number * number;
    }
    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int res = square(n);
        System.out.println(res);
    }
    
}
```

## OUTPUT:
<img width="465" height="142" alt="image" src="https://github.com/user-attachments/assets/21ebd66f-a161-4e8c-8b68-fd6e8796f3ca" />

## RESULT:
The program successfully calculates the square of the given number and returns the correct result.

