# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a class Rectangle using parameterized constructor and calculate area.

## AIM:
To write a Java program that uses a parameterized constructor to initialize the length and width of a rectangle and calculate its area.
## ALGORITHM :
1. Start the program.
2. Import the package `java.util`.
3. Create a class `Rectangle` with attributes `length` and `width`.
4. Define a parameterized constructor to initialize the length and width.
5. Create a method `calculateArea()` to compute and return the area of the rectangle.
6. Create a `Scanner` object to read input values.
7. Read the length and width from the user.
8. Create a `Rectangle` object using the parameterized constructor.
9. Call the `calculateArea()` method using the object.
10. Display the calculated area.
11. End the program.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;
class Rectangle {
    double length;
    double width;
    Rectangle(double length, double width) {
        this.length = length;
        this.width = width;
    }
    double calculateArea() {
        return length * width;
    }
}
public class Main{
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double length = sc.nextDouble();
        double width = sc.nextDouble();
        Rectangle rect = new Rectangle(length, width);
        System.out.println("Area of the rectangle: " + rect.calculateArea());
    }
}
```
## OUTPUT:

<img width="607" height="251" alt="image" src="https://github.com/user-attachments/assets/b2a63a53-fa23-4c56-882e-0cfefb146ea3" />


## RESULT:
The program successfully initializes a rectangle using a parameterized constructor and calculates and displays its area.
