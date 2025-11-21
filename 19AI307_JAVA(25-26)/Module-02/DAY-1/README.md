# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Person with attributes name and age. Write a method greet() that prints: Hello, my name is <name> and I am <age> years old.
<img width="695" height="122" alt="image" src="https://github.com/user-attachments/assets/0363c65e-fe11-41ea-bf95-998c29d44683" />

## AIM:
To create a class Person with attributes name and age. Write a method greet() that prints: Hello, my name is <name> and I am <age> years old.

## ALGORITHM :
1.Start
2.Define a class named Person.
3.Inside the class, create an initializer method __init__() with parameters name and age.
4.Store these parameters into instance variables.
5.Create a method greet() inside the class.
6.In this method, print the message:
"Hello, my name is <name> and I am <age> years old."
7.Create an object of the class Person by passing name and age.
8.Call the greet() method using the object.
9.End.

## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Lokesh Rahul V V 
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class prog 
{
    String name;
    int age;

    prog(String name, int age) 
    {
        this.name = name;
        this.age = age;
    }

    void greet() 
    {
       // Your Code Here
       System.out.println("Hello, my name is "+name+" and I am "+age+" years old.");
    }

    public static void main(String[] args) 
    {
        Scanner scanner = new Scanner(System.in);
        String str = scanner.next();
        int age=scanner.nextInt();
        prog person=new prog(str,age);
        person.greet();
    }


}
```

## OUTPUT:
<img width="1192" height="307" alt="image" src="https://github.com/user-attachments/assets/1924c2ca-5eb2-42ed-9160-0b6354251b02" />


## RESULT:
The program successfully displays the greeting message with the person's name and age.
