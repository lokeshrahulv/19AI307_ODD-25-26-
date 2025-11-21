# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
Create a Super class Person with fields name and age. Create a subclass Student that inherits from Person and adds a field marks (integer). Implement a method in Student called calculateGrade() which returns the grade based on the marks:

Marks ≥ 90: Grade A

Marks ≥ 75 and < 90: Grade B

Marks ≥ 50 and < 75: Grade C

Marks < 50: Grade F

## AIM:
To Create a Super class Person with fields name and age. Create a subclass Student that inherits from Person and adds a field marks (integer). Implement a method in Student called calculateGrade() which returns the grade based on the marks:

## ALGORITHM :
1.Start
2.Create a superclass Person with:

  Variables: name, age

  Constructor to initialize them

3.Create a subclass Student that extends Person and adds:

  Variable: marks

  Constructor to initialize name, age, marks

  Method calculateGrade():

  If marks ≥ 90 → return "A"

  If marks ≥ 80 → return "B"

  If marks ≥ 70 → return "C"

  If marks ≥ 60 → return "D"

  Else return "F"

4.In main():

  Create Student object

  Call calculateGrade()

  Print name, age, marks, and grade

5.End

## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```
## SOURCE CODE:
```
import java.util.Scanner;

// Superclass
class Person {
    String name;
    int age;

    // Constructor
    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Method to display person details
    void displayDetails() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

// Subclass
class Student extends Person {
    int marks;

    // Constructor
    Student(String name, int age, int marks) {
        super(name, age);  // Call parent constructor
        this.marks = marks;
    }

    // Method to calculate grade
    String calculateGrade() {
        if (marks >= 90) {
            return "Grade: A";
        } else if (marks >= 75) {
            return "Grade: B";
        } else if (marks >= 50) {
            return "Grade: C";
        } else {
            return "Grade: F";
        }
    }

    // Display student details
    void displayStudentDetails() {
        displayDetails(); // Call Person method
        System.out.println("Marks: " + marks);
        System.out.println(calculateGrade());
    }
}

// Main class
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Taking input
        String name = sc.nextLine();
        int age = sc.nextInt();
        int marks = sc.nextInt();

        // Create student with input values
        Student s = new Student(name, age, marks);

        // Display details
        s.displayStudentDetails();

        sc.close();
    }
}
```

## OUTPUT:
<img width="535" height="571" alt="image" src="https://github.com/user-attachments/assets/c3c69cf3-ec0b-449c-8e49-38181b83a87d" />

## RESULT:
The program successfully inherits fields from the Person class, adds marks in the Student class, and calculates the student’s grade based on the marks provided.
