# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a Java program to create a new file named example.txt.
<img width="380" height="111" alt="image" src="https://github.com/user-attachments/assets/ae720813-e6c3-4a37-84a0-425c5fcfd38e" />

## AIM:
To Write a Java program to create a new file named example.txt.

## ALGORITHM :
1.Start

2.Create a File object and pass "example.txt" as the filename.

3.Call createNewFile() on the File object:

If the file does not already exist:

The file is created.

Display the message:
"File created: example.txt"

If the file already exists:

4.Display the message:
"File already exists."

5.Use a try–catch block to handle IOException:

If an error occurs, display:
"An error occurred."

6.End


## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.io.File;
import java.io.IOException;

public class CreateFileDemo {
    public static void main(String[] args) {
        try {
            File file = new File("example.txt");

            if (file.createNewFile()) {
                System.out.println("File created: " + file.getName());
            } else {
                System.out.println("File already exists.");
            }

        } catch (IOException e) {
            System.out.println("An error occurred.");
        }
    }
}

```

## OUTPUT:
<img width="724" height="150" alt="Screenshot 2025-11-21 193806" src="https://github.com/user-attachments/assets/2c4d3450-2a3c-4c91-9510-0fb6644c4b47" />

## RESULT:
The program successfully creates a new file named example.txt and prints a confirmation message indicating that the file has been created.
