# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a program to access a static variable using both class name and object.
<img width="617" height="147" alt="image" src="https://github.com/user-attachments/assets/148a1ed8-951c-49dc-a444-59379a1f8e38" />

## AIM:
To Write a program to access a static variable using both class name and object.


## ALGORITHM :
1.Start
2.Create a class with a static variable (e.g., static int count).
3.In the main() method:
4.Access the static variable using the class name.
5.Create an object of the class.
6.Access the same static variable using the object reference.
7.Print values in both cases.
8.End

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.util.*;
class prog{
    static int n;
    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        int num=sc.nextInt();
        prog p=new prog();
        p.n=num;
        System.out.println("Accessing using class name: "+prog.n);
        System.out.println("Accessing using object: "+p.n);
    }
}
```
## OUTPUT:
<img width="836" height="293" alt="image" src="https://github.com/user-attachments/assets/13415bd9-6b7d-4a34-ade7-bdf091ac8a3d" />

## RESULT:
The program successfully accesses the static variable using both the class name and an object, demonstrating that static variables belong to the class rather than individual objects.

