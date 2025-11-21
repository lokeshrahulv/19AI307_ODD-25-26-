# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

Note : Read the threadname from the User

set the priority as 4 for t1 and set the priority as 2 for t2

<img width="531" height="140" alt="image" src="https://github.com/user-attachments/assets/9a2f2af4-f617-4eba-8c24-c9755aead80a" />

## AIM:
To Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

## ALGORITHM :
1.Start

2.Create a Scanner to read two thread names from the user.

3.Create two Thread objects t1 and t2 using the names read.

4.Set priority of:

t1 → 4

t2 → 2

5.Print thread details using toString() → this automatically prints in the format:

6.Thread[name,priority,group]

7.End

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ThreadPriorityDemo {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String name1 = sc.nextLine();  // First thread name
        String name2 = sc.nextLine();  // Second thread name

        Thread t1 = new Thread(name1);
        Thread t2 = new Thread(name2);

        t1.setPriority(4);
        t2.setPriority(2);

        // Print thread details
        System.out.println(t1);
        System.out.println(t2);
    }
}

```

## OUTPUT:
<img width="897" height="231" alt="image" src="https://github.com/user-attachments/assets/f29c19e0-4bcc-400d-a3ce-f0c9f0dde2e7" />

## RESULT:
The program successfully reads two thread names from the user, sets the priority of the first thread to 4 and the priority of the second thread to 2, and then displays the complete thread information in the format:
