# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Create a program that reads a thread name and a priority (1–10), sets that priority to a new thread, prints both values.

 Input:

Two lines: <threadName>, <priority>

 Output:

Thread <threadName> priority set to <priority>
<img width="420" height="132" alt="image" src="https://github.com/user-attachments/assets/328d7950-2585-4681-b147-875ab3e267ea" />

## AIM:
To Create a program that reads a thread name and a priority (1–10), sets that priority to a new thread, prints both values.


## ALGORITHM :
1.Start

2.Read a thread name from the user.

3.Read the priority (1–10) from the user.

4.Create a new Thread object using the provided name.

5.Set the thread priority using setPriority(priority).

6.Print:
Thread <threadName> priority is <priority>

7.End


## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ThreadPrioritySetter {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();
        int priority = sc.nextInt();

        Thread t = new Thread(threadName);
        t.setPriority(priority);

        System.out.println("Thread " + threadName + " priority is " + priority);
    }
}

```
## OUTPUT:
<img width="816" height="293" alt="image" src="https://github.com/user-attachments/assets/3c20bbfd-c571-48d7-8abf-f6ea79214599" />

## RESULT:
The program successfully reads a thread name and a priority value from the user, creates a new thread with the given name, sets its priority to the specified value, and prints the message:
