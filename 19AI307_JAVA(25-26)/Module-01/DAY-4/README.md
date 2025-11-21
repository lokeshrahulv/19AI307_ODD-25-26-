
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

