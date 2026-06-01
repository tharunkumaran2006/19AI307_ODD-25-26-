# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program using method overriding. Create a superclass Bank with a method getInterestRate() returning 0. Create subclasses SBI, ICICI, and HDFC that override the method.

## AIM:
To write a Java program that demonstrates method overriding by creating a superclass `Bank` and subclasses `SBI`, `ICICI`, and `HDFC`, each providing its own interest rate.

## ALGORITHM :
1. Start the program.
2. Create a superclass `Bank` with a method `getInterestRate()` that returns `0`.
3. Create subclasses `SBI`, `ICICI`, and `HDFC` that override the `getInterestRate()` method with their respective interest rates.
4. Create a `Scanner` object to read the bank name from the user.
5. Read the bank name.
6. Based on the input, create an object of the corresponding subclass.
7. Call the overridden `getInterestRate()` method using the object.
8. Display the bank name and its interest rate.
9. If the entered bank name is invalid, display an appropriate error message.
10. End the program.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: THARUN V K 
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

class Bank {
    double getInterestRate() {
        return 0;
    }
}

class SBI extends Bank {
    double getInterestRate() {
        return 6.5;
    }
}

class ICICI extends Bank {
    double getInterestRate() {
        return 7.0;
    }
}

class HDFC extends Bank {
    double getInterestRate() {
        return 7.5;
    }
}

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String bankName = sc.nextLine();

        Bank bank;

        if (bankName.equalsIgnoreCase("SBI")) {
            bank = new SBI();
            System.out.println("SBI Rate: " + bank.getInterestRate() + "%");

        } else if (bankName.equalsIgnoreCase("ICICI")) {
            bank = new ICICI();
            System.out.println("ICICI Rate: " + bank.getInterestRate() + "%");

        } else if (bankName.equalsIgnoreCase("HDFC")) {
            bank = new HDFC();
            System.out.println("HDFC Rate: " + bank.getInterestRate() + "%");
        }
        else{
            System.out.println("Invalid bank name.");
        }

        sc.close();
    }
}
```

## OUTPUT:
<img width="589" height="195" alt="image" src="https://github.com/user-attachments/assets/46503053-1c23-4d60-94d5-457da6fd2dce" />


## RESULT:

The program successfully demonstrates method overriding by displaying different interest rates for SBI, ICICI, and HDFC banks based on the user's input.
