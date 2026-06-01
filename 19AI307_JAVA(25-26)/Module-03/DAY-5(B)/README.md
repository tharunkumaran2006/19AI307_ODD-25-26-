# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to convert a string to an integer using a wrapper class and perform addition.

## AIM:
To write a Java program that converts string values into integers using the `Integer` wrapper class and performs addition on the converted integers.

## ALGORITHM :
1. Start the program.
2. Import the package `java.util`.
3. Create a `Scanner` object to read input.
4. Read two string values from the user.
5. Convert the first string to an integer using `Integer.parseInt()`.
6. Convert the second string to an integer using `Integer.parseInt()`.
7. Add the two integer values.
8. Display the sum.
9. Close the scanner.
10. End the program.

## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str1 = sc.nextLine();
        String str2 = sc.nextLine();
        int num1 = Integer.parseInt(str1);
        int num2 = Integer.parseInt(str2);
        System.out.println("Sum = " + (num1 + num2));
        sc.close();
    }
}
```

## OUTPUT:
<img width="571" height="242" alt="image" src="https://github.com/user-attachments/assets/f010950c-a74e-45ad-a57f-55f78ef0a035" />


## RESULT:
The program successfully converts the input strings into integers using the Integer wrapper class and displays their sum.
