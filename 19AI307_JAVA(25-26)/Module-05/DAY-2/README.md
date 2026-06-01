# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to read a string from the user, compress it in memory using ByteArrayOutputStream + GZIPOutputStream, and then decompress it back using ByteArrayInputStream + GZIPInputStream.

## AIM:
To write a Java program that compresses a user-entered string in memory using ByteArrayOutputStream and GZIPOutputStream, and then decompresses it using ByteArrayInputStream and GZIPInputStream.

## ALGORITHM :
1. Read a string from the user.
2. Compress the string using ByteArrayOutputStream and GZIPOutputStream.
3. Store the compressed data in a byte array.
4. Decompress the byte array using ByteArrayInputStream and GZIPInputStream.
5. Read and reconstruct the original string.
6. Display the compressed data and the decompressed string.
7. Handle exceptions if any occur.
8. End the program.

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.io.*;
import java.util.Scanner;
import java.util.zip.GZIPOutputStream;
import java.util.zip.GZIPInputStream;

public class GZIPMemoryExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        try {
            // Get input string from user
            String input = scanner.nextLine();

            // --- Compress the string ---
            ByteArrayOutputStream baos = new ByteArrayOutputStream();
            GZIPOutputStream gzipOut = new GZIPOutputStream(baos);
            gzipOut.write(input.getBytes("UTF-8"));
            gzipOut.close(); // Finish compression

            byte[] compressedData = baos.toByteArray();
            System.out.println("Compressed data (bytes):");
            for (byte b : compressedData) {
                System.out.print(b + " ");
            }
            System.out.println("\nTotal bytes: " + compressedData.length);

            // --- Decompress the string ---
            ByteArrayInputStream bais = new ByteArrayInputStream(compressedData);
            GZIPInputStream gzipIn = new GZIPInputStream(bais);
            InputStreamReader reader = new InputStreamReader(gzipIn, "UTF-8");
            BufferedReader br = new BufferedReader(reader);

            StringBuilder decompressed = new StringBuilder();
            String line;
            while ((line = br.readLine()) != null) {
                decompressed.append(line);
            }

            System.out.println("\nDecompressed string:");
            System.out.println(decompressed.toString());

        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        }

        scanner.close();
    }
}
```

## OUTPUT:
<img width="1284" height="510" alt="image" src="https://github.com/user-attachments/assets/94ea196e-eda2-4c8f-806e-b7767e485927" />


## RESULT:
The program successfully compresses the input string into a byte array using GZIP compression and then decompresses it back to its original form, displaying both the compressed data and the recovered string.
