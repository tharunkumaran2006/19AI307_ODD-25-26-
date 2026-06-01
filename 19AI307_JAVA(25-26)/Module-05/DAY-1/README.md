# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write characters to a file using FileWriter.

## AIM:
To write a Java program that writes character data to a file using the FileWriter class and displays a success message after writing.

## ALGORITHM :
1. Start the program.
2. Import the required packages java.io and java.util.
3. Create a Scanner object to read input from the user.
4. Read the file name from the user.
5. Read the content to be written into the file.
6. Create a FileWriter object using the specified file name.
7. Write the content to the file using the write() method.
8. Close the FileWriter object to save the data.
9. Display a success message if the file is written successfully.
10. If an exception occurs, display an error message.
11. End the program.

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String fileName = sc.nextLine();
        String content = sc.nextLine();

        try {
            FileWriter writer = new FileWriter(fileName);
            writer.write(content);
            writer.close();

            System.out.println("File written successfully.");
        } catch (IOException e) {
            System.out.println("Error writing file.");
        }
    }
}
```

## OUTPUT:
<img width="777" height="243" alt="image" src="https://github.com/user-attachments/assets/679f1198-417a-4674-92f3-ddde928a6632" />



## RESULT:
The program successfully writes the given character data to the specified file using the FileWriter class and displays an appropriate message indicating the status of the file operation.
