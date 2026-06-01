# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.

However, you're getting a NullPointerException.

What should you check in your array before calling .toUpperCase() on a element?

## AIM:
To write a Java program that checks whether a string is `null` before calling the `toUpperCase()` method and handles null values safely to avoid a `NullPointerException`.

## ALGORITHM :
1. Start the program.
2. Import the package `java.util`.
3. Create a `Scanner` object to read input.
4. Read a string from the user.
5. Check whether the string is `null` or equal to `"null"`.
6. If the condition is true, display **"Null element"**.
7. Otherwise, convert the string to uppercase using `toUpperCase()`.
8. Display the converted string.
9. Close the scanner.
10. End the program.

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
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

        String str = sc.nextLine();

        if (str == null || str.equals("null")) {
            System.out.println("Null element");
        } else {
            System.out.println(str.toUpperCase());
        }

        sc.close();
    }
}
```

## OUTPUT:
<img width="697" height="191" alt="image" src="https://github.com/user-attachments/assets/9a1cbfcd-4be3-463d-98fd-e85b6650538c" />


## RESULT:
The program successfully checks for null values before calling `toUpperCase()` and prevents a `NullPointerException` by displaying an appropriate message when a null element is encountered.
