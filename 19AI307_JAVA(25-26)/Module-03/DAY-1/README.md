# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

finalPrice = purchaseWeight * (goldRatePerGram - discount)

For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).

## AIM:
To write a Java program that uses inheritance to calculate the final gold purchase price for Regular and Premium customers based on discounts and cashback offers.

## ALGORITHM :
1. Start the program.
2. Create a base class `Customer` with attributes: customer ID, name, purchase weight, and gold rate per gram.
3. Define methods to calculate the discount rate and final price.
4. Create a subclass `RegularCustomer` that provides a 2% discount on the gold rate.
5. Create a subclass `PremiumCustomer` that provides a 5% discount and calculates a cashback of 1% of the final price.
6. Read the customer type, customer ID, name, purchase weight, and gold rate per gram from the user.
7. Create an object of `RegularCustomer` or `PremiumCustomer` based on the customer type.
8. Calculate the discount amount and final price.
9. If the customer is Premium, calculate the cashback amount.
10. Display the customer details, discount percentage, final price, and cashback (for Premium customers).
11. End the program.

## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;
import java.text.DecimalFormat;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    int getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");

        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer {

    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    int getDiscountRate() {
        return 2;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");

        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class PremiumCustomer extends Customer {

    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    int getDiscountRate() {
        return 5;
    }

    double calculateCashback() {
        return calculateFinalPrice() * 0.01;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");

        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(calculateCashback()));
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String type = sc.nextLine().trim();

        String customerId = sc.nextLine();
        String name = sc.nextLine();
        double purchaseWeight = sc.nextDouble();
        double goldRatePerGram = sc.nextDouble();

        Customer customer;

        if (type.equalsIgnoreCase("Regular")) {
            customer = new RegularCustomer(customerId, name, purchaseWeight, goldRatePerGram);
        } else {
            customer = new PremiumCustomer(customerId, name, purchaseWeight, goldRatePerGram);
        }

        customer.display();
    }
}
```

## OUTPUT:
<img width="786" height="561" alt="image" src="https://github.com/user-attachments/assets/9b5b5a0e-7f70-4485-a823-03968952033f" />



## RESULT:
The program successfully demonstrates inheritance and method overriding by calculating and displaying the final gold purchase price for Regular and Premium customers, including the cashback benefit for Premium customers.
