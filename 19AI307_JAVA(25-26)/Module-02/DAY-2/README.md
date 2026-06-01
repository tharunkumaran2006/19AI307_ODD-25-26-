# Ex.No:2(B) METHODS

## QUESTION:
Create two methods:

Get the input for radius from the user.

double getArea(double r) → calculate the area and return the area(Don't print anything in this method).

void printArea(double area) → pass the calculated area to this method and print the area of a circle.

## AIM:
To write a Java program that calculates the area of a circle using a method that returns the area and another method that displays the calculated area.

## ALGORITHM :
1. Start the program.
2. Import the package `java.util`.
3. Create a `Scanner` object to read the radius from the user.
4. Read the radius value `r`.
5. Call the method `getArea(r)` to calculate the area of the circle.
6. In `getArea(r)`, compute the area using the formula π × r × r and return the result.
7. Pass the returned area to the method `printArea(area)`.
8. In `printArea(area)`, display the area formatted to two decimal places.
9. End the program.


## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        double r=sc.nextDouble();
        printArea(getArea(r));
    }
    static double getArea(double r){
        return 3.14*r*r;
    }
    static void printArea(double area){
        System.out.printf("%.2f",area);
    }
}
```

## OUTPUT:
<img width="292" height="126" alt="image" src="https://github.com/user-attachments/assets/8f6cb1b0-fbff-4c2d-bf04-402f34404e33" />


## RESULT:
The program successfully calculates the area of a circle using a method and displays the result using another method.
