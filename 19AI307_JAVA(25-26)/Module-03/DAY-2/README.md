# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator with:
  area(int side) for square

  area(int length, int breadth) for rectangle

  area(double radius) for circle
<img width="452" height="333" alt="image" src="https://github.com/user-attachments/assets/b3b1e0ac-e708-4dc2-8168-bd520cb9641f" />

## AIM:
To Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator with:

## ALGORITHM :
1.Start

2.Create a class AreaCalculator.

3.Overload the method area() in the following ways:

   area(int side) → calculate area of a square using side × side.
   
   area(int length, int breadth) → calculate area of a rectangle.
   
   area(double radius) → calculate area of a circle using π × r².

4.In the main() method:

   Create an object of AreaCalculator.
   
   Call each overloaded method.
   
   Print the results.

5.End



## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class AreaCalculator {
    // Area of square
    int area(int side) {
        return side * side;
    }

    // Area of rectangle
    int area(int length, int breadth) {
        return length * breadth;
    }

    // Area of circle
    double area(double radius) {
        return Math.PI * radius * radius;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        AreaCalculator calculator = new AreaCalculator();

        // Input for square
        int side = sc.nextInt();
        System.out.println("Area of square: " + calculator.area(side));

        // Input for rectangle
        int length = sc.nextInt();
        int breadth = sc.nextInt();
        System.out.println("Area of rectangle: " + calculator.area(length, breadth));

        // Input for circle
        double radius = sc.nextDouble();
        System.out.println("Area of circle: " + calculator.area(radius));

        sc.close();
    }
}
```

## OUTPUT:
<img width="877" height="366" alt="image" src="https://github.com/user-attachments/assets/3d418765-ba2a-416f-9964-14ce43a1ebab" />

## RESULT:
The program successfully calculates the areas of different shapes (square, rectangle, and circle) using method overloading and displays the correct results.



