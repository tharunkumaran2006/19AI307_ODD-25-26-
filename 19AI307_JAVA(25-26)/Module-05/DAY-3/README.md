# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to count the number of characters in a file.

## AIM:
To write a Java program that writes text to a file and counts the number of characters present in the file using FileWriter and FileReader.

## ALGORITHM :
1. Read a string from the user.
2. Create a file and write the string into it using FileWriter.
3. Open the file using FileReader.
4. Read the file character by character.
5. Count each character until the end of the file is reached.
6. Display the total number of characters.
7. Handle any input/output exceptions.
8. End the program.

## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.io.FileWriter;
import java.io.FileReader;
import java.io.IOException;
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String text = sc.nextLine();
        String fileName = "sample.txt";
        try {
            FileWriter writer = new FileWriter(fileName);
            writer.write(text);
            writer.close();
            FileReader reader = new FileReader(fileName);
            int count = 0;
            while (reader.read() != -1) {
                count++;
            }
            reader.close();
            System.out.println("Number of characters written to the file: " + count);
        } 
        catch (IOException e) {
            System.out.println("Error");
        }
        sc.close();
    }
}
```

## OUTPUT:
<img width="919" height="195" alt="image" src="https://github.com/user-attachments/assets/847fcba4-9e2b-464a-b62b-7209f5a222f4" />


## RESULT:
The program successfully writes the given text to a file, reads it back character by character, and displays the total number of characters present in the file.
