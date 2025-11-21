# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to read multiple UTF strings from the user, write them to a ByteArrayOutputStream using DataOutputStream, and display the byte array contents.

<img width="753" height="270" alt="image" src="https://github.com/user-attachments/assets/9681f0b5-371d-4e83-a5bc-26a83a14c5aa" />

## AIM:
To Write a Java program to read multiple UTF strings from the user, write them to a ByteArrayOutputStream using DataOutputStream, and display the byte array contents.

## ALGORITHM :
1.Start

2.Create a Scanner to read input from the user.

3.Create a ByteArrayOutputStream object (memory buffer).

Wrap it inside DataOutputStream (to write UTF strings).

4.Read how many strings the user wants to enter.

5.Loop for each string:

6.Read string input

7.Write it using writeUTF() into the DataOutputStream

8.After writing all strings, call toByteArray() on ByteArrayOutputStream to get the raw byte array.

9.Display the byte values.

10.Close all streams.

11.End

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.Scanner;

public class UTFStringsInMemoryUserInput 
{
    public static void main(String[] args) 
    {
        Scanner scanner = new Scanner(System.in);

        try 
        {
            ByteArrayOutputStream baos = new ByteArrayOutputStream();
            DataOutputStream dos = new DataOutputStream(baos);
            int n = scanner.nextInt();
            scanner.nextLine(); 
            for (int i = 0; i < n; i++) 
            {
                String str = scanner.nextLine();
                dos.writeUTF(str);
            }
            byte[] byteData = baos.toByteArray();
            System.out.println("Byte array contents:");
            for (byte b : byteData) 
            {
                System.out.print(b + " ");
            }
            System.out.println("\nTotal bytes: " + byteData.length);
            ByteArrayInputStream bais = new ByteArrayInputStream(byteData);
            DataInputStream dis = new DataInputStream(bais);
            System.out.println("\nStrings read from memory:");
            for(int i=0;i<n;i++)
            {
                String readStr = dis.readUTF();
                System.out.println(readStr);
            }
        }
        catch(Exception e)
        {
            System.out.println("Error: "+e.getMessage());
        }
    }
}

```

## OUTPUT:
<img width="1188" height="690" alt="image" src="https://github.com/user-attachments/assets/9c09608a-9c94-4c47-9423-718aff536412" />

## RESULT:
The program successfully:

Reads multiple UTF strings from the user

Writes them into a ByteArrayOutputStream via DataOutputStream.writeUTF()

Converts the stored data into a raw byte array

Prints every byte value to the console

This demonstrates storing UTF-encoded text in memory and inspecting its binary representation.
