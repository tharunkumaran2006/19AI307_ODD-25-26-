# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a java program to replace each space with a hyphen.

## AIM:
To write a java program to replace each space with a hyphen.

## ALGORITHM :
1. Start the program.
2. Import the package `java.util`.
3. Create a `Scanner` object to read input.
4. Read a string from the user.
5. Replace all spaces in the string with hyphens using the `replace()` method.
6. Store the modified string in a variable.
7. Display the modified string.
8. End the program.

## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
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

        String str = sc.nextLine();
        String result = str.replace(' ', '-');

        System.out.println("Modified string: " + result);
    }
}
```

## OUTPUT:
<img width="747" height="269" alt="image" src="https://github.com/user-attachments/assets/24422d38-65c8-41ca-bff6-10bd2e8aaa83" />



## RESULT:
The program successfully replaces all spaces in the given string with hyphens and displays the modified string.
