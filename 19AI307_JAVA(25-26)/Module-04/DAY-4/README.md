# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create a program that sends different types of notifications: "email", "sms", and "push". Use the Factory Pattern to generate the appropriate notification sender and call its notifyUser() method.

## AIM:
To write a Java program that implements the Factory Design Pattern to create different types of notification objects and send notifications using the `notifyUser()` method.

## ALGORITHM :
1. Start the program.
2. Create an interface `Notification` with the method `notifyUser()`.
3. Create classes `EmailNotification`, `SMSNotification`, and `PushNotification` that implement the `Notification` interface.
4. Override the `notifyUser()` method in each class to display the corresponding notification message.
5. Create a `NotificationFactory` class with a method `createNotification()`.
6. In the factory method, create and return the appropriate notification object based on the input type.
7. Create a `Scanner` object to read user input.
8. Create an object of `NotificationFactory`.
9. Continuously read the notification type from the user.
10. If the input is `"exit"`, terminate the loop.
11. Use the factory method to create the required notification object.
12. If a valid object is returned, call its `notifyUser()` method.
13. Otherwise, display an invalid notification type message.
14. End the program.

## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

interface Notification {
    void notifyUser();
}

class EmailNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Email Notification");
    }
}

class SMSNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending SMS Notification");
    }
}

class PushNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Push Notification");
    }
}

class NotificationFactory {

    public Notification createNotification(String type) {

        if (type.equalsIgnoreCase("email")) {
            return new EmailNotification();
        } else if (type.equalsIgnoreCase("sms")) {
            return new SMSNotification();
        } else if (type.equalsIgnoreCase("push")) {
            return new PushNotification();
        }

        return null;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        NotificationFactory factory = new NotificationFactory();

        while (true) {
            String input = sc.nextLine();

            if (input.equalsIgnoreCase("exit")) {
                break;
            }

            Notification n = factory.createNotification(input);

            if (n != null) {
                n.notifyUser();
            } else {
                System.out.println("Invalid notification type: " + input);
            }
        }

        sc.close();
    }
}
```


## OUTPUT:
<img width="631" height="247" alt="image" src="https://github.com/user-attachments/assets/ac119cbc-09d1-48ab-9390-2a51cb53feb0" />


## RESULT:
The program successfully demonstrates the Factory Design Pattern by creating different notification objects based on user input and invoking the appropriate `notifyUser()` method to send notifications.
