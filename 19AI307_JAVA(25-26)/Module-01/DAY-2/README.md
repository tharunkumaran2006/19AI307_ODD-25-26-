# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
Aliens scan DNA numbers:

If the DNA number is divisible by 2 and ends in 4, they accept it.

If the DNA number is divisible by 2 but ends in anything else, it’s a suspect.

If the DNA is odd, they reject it.

The program will print one of the following statements based on the input:

Accepted
Suspect
Rejected

## AIM:
To write a Java program that checks a DNA number and classifies it as Accepted, Suspect, or Rejected based on its divisibility by 2 and its last digit.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read an integer value n from the user.
4. Determine whether the number is even by checking if it is divisible by 2.
5. Determine the last digit of the number by finding the remainder when divided by 10.
6. Check if the number is divisible by 4 and its last digit is 4.
7. If both conditions are true, classify the DNA number as Accepted and display "Accepted".
8. Otherwise, check if the number is divisible by 2.
9. If the number is even, classify it as Suspect and display "Suspect".
10. If the number is not divisible by 2, classify it as Rejected and display "Rejected".
11. Display the corresponding classification result.





## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        if(n%4==0 && n%10==4){
            System.out.println("Accepted");
        }
        else if(n%2==0){
            System.out.println("Suspect");
        }
        else{
            System.out.println("Rejected");
        }
    }
}
```






## OUTPUT:
<img width="465" height="266" alt="image" src="https://github.com/user-attachments/assets/5a6f042a-7c18-4f45-8ddb-56af12b4c48e" />



## RESULT:
The program successfully reads a DNA number and classifies it as Accepted, Suspect, or Rejected based on the given conditions of divisibility and the last digit of the number.
