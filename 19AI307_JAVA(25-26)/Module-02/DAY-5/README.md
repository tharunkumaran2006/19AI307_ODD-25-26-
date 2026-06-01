# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".

## AIM:
To write a Java program that creates a class `Calculator` with a non-static method to add two numbers and a static method to display a readiness message.

### ALGORITHM
1. Start the program.
2. Import the package `java.util`.
3. Create a class `Calculator`.
4. Define a non-static method `add(int a, int b)` that returns the sum of two numbers.
5. Define a static method `info()` that displays the message **"Calculator is ready"**.
6. Create a `Scanner` object to read input values.
7. Read two integers from the user.
8. Create an object of the `Calculator` class.
9. Call the `add()` method using the object and store the result.
10. Call the static `info()` method using the class name.
11. Display the sum of the two numbers.
12. End the program.

## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

class Calculator {
    int add(int num1,int num2){
        return num1+num2;
    }
    static void info(){
        System.out.println("Calculator is ready");
    }
}
class prog {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int num1=sc.nextInt();
        int num2=sc.nextInt();
        Calculator c=new Calculator();
        int sum=c.add(num1,num2);
        Calculator.info();
        System.out.println("Sum: "+sum);
    }
}

```

## OUTPUT:
<img width="531" height="244" alt="image" src="https://github.com/user-attachments/assets/7e7dbfd3-2392-4762-b586-849d6b815591" />



## RESULT:
The program successfully demonstrates the use of both non-static and static methods by calculating the sum of two numbers and displaying a readiness message.
