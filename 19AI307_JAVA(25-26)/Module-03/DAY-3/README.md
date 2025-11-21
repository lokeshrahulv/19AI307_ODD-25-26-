# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create an abstract class Employee with method calculatePay(). Extend it to HourlyEmployee and SalariedEmployee.

## AIM:
Create an abstract class Employee with method calculatePay(). Extend it to HourlyEmployee and SalariedEmployee.

## ALGORITHM :
1.Start
2.Create an abstract class Employee with:
3.Abstract method calculatePay()
4.Create HourlyEmployee subclass:
5.Create SalariedEmployee subclass:
6.Implement calculatePay() → return monthlySalary
7.Create objects of each type
8.Print the results
9.End

## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:

```
import java.util.*;
abstract class Employee 
{
    abstract void calculatePay();
}

class HourlyEmployee extends Employee 
{
    int hours;
    double pay;

    HourlyEmployee(int a, double b) 
    {
        this.hours = a;
        this.pay = b;
    }

    void calculatePay() 
    {
        System.out.printf("%.2f", hours * pay);
    }
}

class SalariedEmployee extends Employee 
{
    double salary;

    SalariedEmployee(double a) 
    {
        this.salary = a;
    }

    void calculatePay() 
    {
        System.out.printf("%.2f", salary);
    }
}

class prog {
    public static void main(String[] args) 
    {
        Scanner in = new Scanner(System.in);
        int type = in.nextInt();
        if (type == 1) 
        { 
            int duration = in.nextInt();
            double payment = in.nextDouble();
            HourlyEmployee emp = new HourlyEmployee(duration, payment);
            emp.calculatePay();
        } 
        else 
        {
            double payment = in.nextDouble();
            SalariedEmployee emp = new SalariedEmployee(payment);
            emp.calculatePay();
        }
    }
}

```

## OUTPUT:
<img width="375" height="217" alt="image" src="https://github.com/user-attachments/assets/4860ccd9-7775-4403-b94f-a0e43a57ba8e" />

## RESULT:
The program successfully calculates pay for both types of employees using polymorphism. HourlyEmployee computes pay based on hours and rate, while SalariedEmployee returns a fixed monthly salary.
