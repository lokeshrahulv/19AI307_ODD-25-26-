# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You are asked to simulate a simple Shape Drawing Tool using the Factory Design Pattern in Java.

You will implement a Shape interface with concrete classes for different shapes (Circle, Square, Rectangle). Using a ShapeFactory, your program will take shape names from user input and draw them accordingly. If the shape is unknown, print an error message.

Requirements:
Create a Shape interface with a draw() method.

Implement Circle, Square, and Rectangle classes that implement Shape and override the draw() method to print a specific message.

Implement a ShapeFactory class that returns the correct shape instance based on input.

In your main method, continuously read shape names from the user (using Scanner) until they type "exit" (case-insensitive).

For each valid shape name, create the shape and call draw().

For invalid shapes, print: Invalid shape: <name>
<img width="360" height="197" alt="image" src="https://github.com/user-attachments/assets/e893179c-d5d1-4db8-8b19-bf7c9405fbb0" />

## AIM:
To simulate a simple Shape Drawing Tool using the Factory Design Pattern in Java, where the user enters shape names, and the program creates the appropriate shape object and draws it. If the shape is unknown, the program displays an error message.

## ALGORITHM :
1.Start

2.Create a Shape interface with a method draw().

3.Create concrete classes:

   Circle

   Square

   Rectangle

4.Each class implements Shape and prints a specific message in draw().

5.Create a ShapeFactory class:

6.Implement a getShape(String shapeName) method.

7.Based on shapeName (case-insensitive), return:

   new Circle()

   new Square()

   new Rectangle()

8.If no match, return null.

9.In main():

Use Scanner to read user input continuously.

If user enters "exit" (case-insensitive), stop the loop.

Pass the input to the factory.

If factory returns a shape → call draw()

Else → print: Invalid shape: <name>

10.End


## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Lokesh Rahul V V 
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface Shape {
    void draw();
}

class Circle implements Shape {
    @Override
    public void draw() {
        System.out.println("Drawing Circle");
    }
}

class Square implements Shape {
    @Override
    public void draw() {
        System.out.println("Drawing Square");
    }
}

class Rectangle implements Shape {
    @Override
    public void draw() {
        System.out.println("Drawing Rectangle");
    }
}

class ShapeFactory {
    public Shape getShape(String shapeName) {
        if (shapeName == null) return null;

        switch (shapeName.toLowerCase()) {
            case "circle":
                return new Circle();
            case "square":
                return new Square();
            case "rectangle":
                return new Rectangle();
            default:
                return null;
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ShapeFactory factory = new ShapeFactory();

        while (true) {
            String input = sc.nextLine();

            if (input.equalsIgnoreCase("exit"))
                break;

            Shape shape = factory.getShape(input);

            if (shape != null) {
                shape.draw();
            } else {
                System.out.println("Invalid shape: " + input);
            }
        }
    }
}

```

## OUTPUT:
<img width="735" height="452" alt="image" src="https://github.com/user-attachments/assets/118b7a57-fd8d-45fe-bf1e-ba8d6d986b06" />

## RESULT:
The program successfully uses the Factory Design Pattern to create and draw shapes based on user input.
Valid shapes display drawing messages, while invalid inputs show an error message.
Typing exit stops the program.
