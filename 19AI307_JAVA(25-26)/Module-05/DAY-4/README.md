# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

Note : Read the threadname from the User

set the priority as 4 for t1 and set the priority as 2 for t2

## AIM:
To write a Java program that creates two threads, assigns user-defined names to them, sets their priorities, and displays the thread details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the names of two threads from the user.
4.	Create two thread objects t1 and t2.
5.	Set the name of t1 using the first input.
6.	Set the name of t2 using the second input.
7.	Set the priority of t1 to 4.
8.	Set the priority of t2 to 2.
9.	Display the details of both threads.
10.	Close the scanner.
11.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
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
        String name1 = sc.nextLine();
        String name2 = sc.nextLine();
        Thread t1 = new Thread();
        Thread t2 = new Thread();
        t1.setName(name1);
        t2.setName(name2);
        t1.setPriority(4);
        t2.setPriority(2);
        System.out.println(t1);
        System.out.println(t2);
        sc.close();
    }
}
```

## OUTPUT:
<img width="685" height="188" alt="image" src="https://github.com/user-attachments/assets/17d7ffa5-645c-4250-b396-dd7049b3598b" />


## RESULT:
The program successfully creates two threads, assigns user-specified names, sets their priorities to 4 and 2 respectively, and displays the thread information.
