# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Smartphone with private instance variables brand, model, and storageCapacity. Provide public getter and setter methods to access and modify these variables. Add a method called increaseStorage() that takes an integer value and increases the storageCapacity by that value.

## AIM:
To Write a Java program to create a class called Smartphone with private instance variables brand, model, and storageCapacity. Provide public getter and setter methods to access and modify these variables. Add a method called increaseStorage() that takes an integer value and increases the storageCapacity by that value.

## ALGORITHM :
1.Start

2.Create a class Smartphone with private variables brand, model, storageCapacity.

3.Provide getter and setter methods for each variable.

4.Create increaseStorage(int value) to add the value to storageCapacity if value > 0.

5.In main():

6.Create a Scanner

7.Take user input for brand, model, and storage

8.Take input for value to increase storage

9.Call increaseStorage()

10.Display updated details

11.End


## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Smartphone {
    private String brand;
    private String model;
    private int storageCapacity;

    public String getBrand() {
        return brand;
    }

    public String getModel() {
        return model;
    }

    public int getStorageCapacity() {
        return storageCapacity;
    }

    public void setBrand(String brand) {
        this.brand = brand;
    }

    public void setModel(String model) {
        this.model = model;
    }

    public void setStorageCapacity(int storageCapacity) {
        this.storageCapacity = storageCapacity;
    }

    public void increaseStorage(int value) {
        if (value > 0) {
            this.storageCapacity += value;
        }
    }

    public void display() {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Updated Storage Capacity: " + storageCapacity + " GB");
        System.out.println("------------------------------");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Smartphone phone = new Smartphone();

        phone.setBrand(sc.nextLine());

        phone.setModel(sc.nextLine());

        phone.setStorageCapacity(sc.nextInt());

        int value = sc.nextInt();

        phone.increaseStorage(value);

        phone.display();
    }
}

```

## OUTPUT:
<img width="1011" height="443" alt="image" src="https://github.com/user-attachments/assets/93d278dc-49f9-469c-b006-ab6b4504f614" />

## RESULT:
The program successfully accepts smartphone details from the user, increases the storage capacity by the specified amount, and displays the updated information.

