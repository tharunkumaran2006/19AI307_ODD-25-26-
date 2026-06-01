# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Use a thread pool to calculate and print the square of each number from input.

## AIM:
To write a Java program that uses a thread pool to calculate and print the square of each input number concurrently.

## ALGORITHM :
1. Read the number of elements `n` from the user.
2. Create a fixed thread pool with two threads using `ExecutorService`.
3. Create a list to store the results of submitted tasks.
4. Read each number from the user.
5. Submit a task to the thread pool that calculates the square of the number.
6. Store the returned `Future` object in the list.
7. Retrieve the result from each `Future` object using `get()`.
8. Display the square of each number.
9. Shut down the thread pool.
10. Close the scanner.
11. End the program.

## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.*;
import java.util.concurrent.*;

public class Main {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        ExecutorService pool = Executors.newFixedThreadPool(2);

        List<Future<Integer>> results = new ArrayList<>();

        for (int i = 0; i < n; i++) {
            int num = sc.nextInt();

            results.add(pool.submit(() -> num * num));
        }

        for (Future<Integer> f : results) {
            System.out.println("Square: " + f.get());
        }

        pool.shutdown();
        sc.close();
    }
}
```

## OUTPUT:
<img width="852" height="362" alt="image" src="https://github.com/user-attachments/assets/c220e862-33bf-49f3-bf13-f022aef65b04" />


## RESULT:
The program successfully uses a thread pool to perform concurrent computation of squares and displays the square of each input number.
