# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an enum Season with values WINTER, SPRING, SUMMER, and FALL. Use a switch statement to display a custom message based on the current season.
<img width="542" height="385" alt="image" src="https://github.com/user-attachments/assets/838e9c98-d343-4647-9496-78aac9aa41ee" />

## AIM:
To write a Java program to create an enum Season with values WINTER, SPRING, SUMMER, and FALL. Use a switch statement to display a custom message based on the current season.

## ALGORITHM :
1.Start

2.Create an enum Season with values:

   WINTER, SPRING, SUMMER, FALL

3.Read a season name from the user

4.Convert the input string to uppercase so it matches enum names.

  Use Season.valueOf() to convert the string to an enum value.

5.Use a switch statement:

  If WINTER → print “It's cold outside. Stay warm!”
  
  If SPRING → print “Flowers are blooming. Enjoy the fresh air!”
  
  If SUMMER → print “It's sunny and hot. Time for the beach!”
  
  If FALL → print “Leaves are falling. Autumn is beautiful!”

6.Display the output.

7.End

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
enum Season
{
    WINTER, SPRING, SUMMER, FALL
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine().toUpperCase();  // Convert to uppercase
        Season season = Season.valueOf(input);  // Convert string to enum
        switch (season) {
            case WINTER:
                System.out.println("It's cold outside. Stay warm!");
                break;

            case SPRING:
                System.out.println("Flowers are blooming. Enjoy the fresh air!");
                break;

            case SUMMER:
                System.out.println("It's sunny and hot. Time for the beach!");
                break;

            case FALL:
                System.out.println("Leaves are falling. Autumn is beautiful!");
                break;
        }
    }
}
```
## OUTPUT:
<img width="997" height="237" alt="image" src="https://github.com/user-attachments/assets/8d2d5419-4a1e-4457-ac02-7e26c71c926e" />

## RESULT:
The program successfully reads the season from the user, converts it to an enum value, and displays the correct custom message using a switch statement.


