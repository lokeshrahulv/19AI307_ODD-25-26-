# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).
<img width="523" height="292" alt="image" src="https://github.com/user-attachments/assets/469da410-2855-4f88-813c-fe04d50d2630" />

## AIM:
To Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

## ALGORITHM :
1.Start

2.Create a Book class with:

3.Fields: title, author

4.Constructor to initialize them

5.Create a Library class with:

6.A private list/array of Books

7.A method addBook(title, author) that:

8.Creates a new Book object

9.Stores it inside the Library (Composition)

10.A method displayBooks() to print the list of stored books

11.In main():

12.Read number of books, n

For each book:

Read title

Read author

Add the book to the Library

Print:

Books in Library:
- title by author


13.End

## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.util.*;

class Book {
    private String title;
    private String author;

    // Book is created only inside Library → Composition
    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return "- " + title + " by " + author;
    }
}

class Library {
    private ArrayList<Book> books = new ArrayList<>();

    // Composition: Book created inside Library
    public void addBook(String title, String author) {
        Book book = new Book(title, author);
        books.add(book);
    }

    public void displayBooks() {
        System.out.println("Books in Library:");
        for (Book b : books) {
            System.out.println(b.getDetails());
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine(); // consume newline

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.displayBooks();
    }
}

```

## OUTPUT:
<img width="902" height="525" alt="image" src="https://github.com/user-attachments/assets/0e678f73-79d8-496d-b4c5-0b33274916a4" />

## RESULT:
The program successfully demonstrates Composition by creating Book objects only inside the Library class.
