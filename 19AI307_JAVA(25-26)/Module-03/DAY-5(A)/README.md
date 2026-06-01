# Ex.No:3(E) INNER CLASS

## QUESTION:
 Write a Java program where the inner class is declared private and accessed through a method in the outer class.

## AIM:
To write a Java program that demonstrates the use of a private inner class and accesses it through a method of the outer class.

## ALGORITHM :
1. Start the program.
2. Create an outer class `Outer`.
3. Declare a private inner class `Inner` inside the `Outer` class.
4. Define a method `display()` in the inner class to display the given data.
5. Define a method `accessInner()` in the outer class.
6. Inside `accessInner()`, create an object of the private inner class.
7. Call the `display()` method using the inner class object.
8. Create a `Scanner` object to read input from the user.
9. Read an integer value.
10. Create an object of the `Outer` class.
11. Call the `accessInner()` method and pass the input value.
12. Display the output from the private inner class.
13. End the program.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: THARUN V K 
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;
class Outer {
    private class Inner {
        void display(int data) {
            System.out.println("Data set inside private inner class: " + data);
        }
    }
    void accessInner(int value) {
        Inner obj = new Inner();
        obj.display(value);
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        Outer outer = new Outer();
        outer.accessInner(n);
        sc.close();
    }
}
```

## OUTPUT:
<img width="813" height="191" alt="image" src="https://github.com/user-attachments/assets/9a18112f-8d3a-4ad6-bdcf-796d9c70327d" />



## RESULT:
The program successfully demonstrates a private inner class and shows how it can be accessed indirectly through a method of the outer class.
