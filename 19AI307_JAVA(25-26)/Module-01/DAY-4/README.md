# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java Program to Find the Average of Array Elements.

## AIM:
To write a Java Program to Find the Average of Array Elements.

## ALGORITHM :
1. Start the program.
2. Import the package java.util.
3. Create a Scanner object to read input.
4. Read the number of elements n.
5. Initialize a variable sum to 0.
6. Use a loop to read n elements and add each element to sum.
7. Calculate the average using average = sum / n.
8. Display the average value formatted to two decimal places.
9. End the program.





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        double sum = 0;

        for (int i = 0; i < n; i++) {
            sum += sc.nextInt();
        }

        double avg = sum / n;

        System.out.printf("The average of elements is %.2f", avg);
    }
}
```






## OUTPUT:
<img width="784" height="460" alt="image" src="https://github.com/user-attachments/assets/6cd8d47e-8fb5-43de-b578-f11481626981" />



## RESULT:
The program successfully calculates and displays the average of the given set of numbers up to two decimal places.
