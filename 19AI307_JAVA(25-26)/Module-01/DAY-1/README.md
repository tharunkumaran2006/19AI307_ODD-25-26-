# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely is preparing a countdown for her rocket launch game. She has a starting number and wants to understand how subtracting with -- works in Java. But she's puzzled by the two types:

Post-decrement (a--) → value is used first, then decreased

Pre-decrement (--a) → value is decreased first, then used

To complete the launch program, help Lovely:

Take a countdown number as input.

Apply both post-decrement and pre-decrement on it.

Show how the value changes in each case.

## AIM:
To write a Java program that demonstrates the use of variables, data types, operators, and different print statements (print, println, and printf).

## ALGORITHM :
1.Read an integer value a from the user.

2.Display the initial value of a.

3.Perform post-decrement (a--) and store the result in post.

4.Display the value of post and the current value of a.

5.Perform pre-decrement (--a) and store the result in pre.

6.Display the value of pre and the current value of a.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: THARUN V K 
RegisterNumber:  212223230231
*/
```

## Sourcecode.java:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        System.out.println("Initial countdown = " + a);
        int post = a--;
        System.out.println("After post-decrement (a--) = " + post + ", Now a = " + a);
        int pre = --a;
        System.out.println("After pre-decrement (--a) = " + pre + ", Now a = " + a);
    }
}
```






## OUTPUT:
<img width="1099" height="298" alt="image" src="https://github.com/user-attachments/assets/33687843-121b-4b6d-8092-0d3c48620cd9" />



## RESULT:
The program demonstrates the difference between post-decrement (a--) and pre-decrement (--a) operators by displaying their returned values and the updated value of the variable after each operation.
