# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to demonstrate chaining of streams (BufferedReader on top of InputStreamReader on top of System.in)
<img width="456" height="175" alt="image" src="https://github.com/user-attachments/assets/e5a0faab-f954-4ae8-9455-425cfb6652fa" />

## AIM:
To Write a program to demonstrate chaining of streams (BufferedReader on top of InputStreamReader on top of System.in)

## ALGORITHM :
1.Start

2.Display a message asking the user to enter text.

3.Create a BufferedReader object chained as:

System.in (byte input stream)

wrapped inside InputStreamReader (converts bytes → characters)

wrapped inside BufferedReader (adds buffering + readLine())

4.Read a line of text using readLine().

5.Print the text back to the user.

6.Handle IOException if any error occurs.

7.End

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class ChainingStreamsExample 
{
    public static void main(String[] args) throws IOException
    {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String name = br.readLine();
        int age = Integer.parseInt(br.readLine());
        System.out.println("--- User Details ---");
        System.out.println("Name: "+name);
        System.out.println("Age: "+age);
    }
}
```

## OUTPUT:
<img width="582" height="467" alt="image" src="https://github.com/user-attachments/assets/d993fb00-4617-45c3-bf47-5357acd05777" />

## RESULT:
The program successfully demonstrates stream chaining by placing a BufferedReader on top of an InputStreamReader, which is itself built over System.in.


