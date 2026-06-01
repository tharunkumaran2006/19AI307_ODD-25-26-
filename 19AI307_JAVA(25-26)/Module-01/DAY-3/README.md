# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
A prime number is a number greater than 1 that has no divisors other than 1 and itself. For example:

2, 3, 5, and 7 are prime numbers.

4, 6, and 9 are not prime numbers because they have divisors other than 1 and themselves.

Write a Java program that:

Prompts the user to enter a positive integer.

Checks whether the entered number is prime or not.

Uses a loop to test divisibility from 2 up to the square root of the number.

Displays a clear message indicating whether the number is prime or not.

## AIM:
To write a Java program that checks whether a given positive integer is a prime number by testing its divisibility from 2 up to the square root of the number and displays the appropriate result.

## ALGORITHM :
1. Start the program.
2. Import the package java.util.
3. Create a Scanner object and read an integer n.
4. Initialize a boolean variable isPrime as true.
5. Check if n <= 1; if true, set isPrime to false.
6. Otherwise, use a loop from 2 to √n to check divisibility.
7. If n is divisible by any number in the loop, set isPrime to false and exit the loop.
8. Check the value of isPrime.
9. If isPrime is true, display that the number is a prime number; otherwise, display that it is not a prime number.
10. End the program.




## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
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
        boolean isPrime = true;

        if (n <= 1) {
            isPrime = false;
        } else {
            for (int i = 2; i <= Math.sqrt(n); i++) {
                if (n % i == 0) {
                    isPrime = false;
                    break;
                }
            }
        }

        if (isPrime) {
            System.out.println(n + " is a Prime number.");
        } else {
            System.out.println(n + " is not a Prime number.");
        }
    }
}
```






## OUTPUT:
<img width="1334" height="264" alt="image" src="https://github.com/user-attachments/assets/87ac97ca-ce1e-4478-a13f-d4b545acae56" />



## RESULT:
The program successfully determines whether the given positive integer is a prime number by checking its divisibility up to its square root and displays the corresponding result.
