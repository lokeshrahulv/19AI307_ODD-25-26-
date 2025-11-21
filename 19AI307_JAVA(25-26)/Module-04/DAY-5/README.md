# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Design a program where a Product model stores item info, and the view displays it. Implement a controller to update product price and refresh the view automatically.

## AIM:
To Design a program where a Product model stores item info, and the view displays it. Implement a controller to update product price and refresh the view automatically.

## ALGORITHM :
1.Start

2.Create a Product (Model) class with:

Fields: name, price

Getters & setters

3.Create a ProductView class that:

Contains a method displayProduct(name, price) to print product info.

4.Create a ProductController class that:

5.Holds references to Product and ProductView

Methods:

updatePrice(double newPrice)

refreshView() → calls view’s display method

In main():

6.Create a Product (model)

7.Create a ProductView

8.Create a ProductController with model + view

9.Display initial product details

10.Update price using controller → automatically refresh view

11.End


## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.util.*;

class Product {
    private String name;
    private double price;
    private String code;

    public Product(String name, double price, String code) {
        this.name = name;
        this.price = price;
        this.code = code;
    }

    public String getName() { return name; }
    public double getPrice() { return price; }
    public String getCode() { return code; }

    public void setPrice(double price) { this.price = price; }
}

class ProductView {
    public void display(String name, double price, String code) {
        System.out.println("--- Product Details ---");
        System.out.println("Name : " + name);
        System.out.println("Price: " + price);
        System.out.println("Code : " + code);
    }
}

class ProductController {
    private Product model;
    private ProductView view;

    public ProductController(Product model, ProductView view) {
        this.model = model;
        this.view = view;
    }

    public void updatePrice(double newPrice) {
        model.setPrice(newPrice);
        refreshView();
    }

    public void refreshView() {
        view.display(model.getName(), model.getPrice(), model.getCode());
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();
        double price1 = Double.parseDouble(sc.nextLine());
        String code = sc.nextLine();
        double price2 = Double.parseDouble(sc.nextLine());

        Product product = new Product(name, price1, code);
        ProductView view = new ProductView();
        ProductController controller = new ProductController(product, view);

        controller.refreshView();      // First display
        controller.updatePrice(price2); // Update & display again
    }
}

```

## OUTPUT:
<img width="747" height="323" alt="Screenshot 2025-11-21 192747" src="https://github.com/user-attachments/assets/dedc4377-cb22-4e21-8862-11deaf4bb878" />

## RESULT:
The MVC system works successfully:

The Model stores the product data.

The View displays the data.

The Controller updates the product price.

Every time the price is updated, the view automatically refreshes and displays the updated information.
