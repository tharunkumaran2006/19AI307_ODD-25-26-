# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Person with private instance variables name, age. and country. Provide public getter and setter methods to access and modify these variables.

## AIM:
To write a Java program that creates a class `Person` with private instance variables `name`, `age`, and `country`, and uses public getter and setter methods to access and modify these variables.

### ALGORITHM
1. Start the program.
2. Import the package `java.util`.
3. Create a class `Person` with private variables `name`, `age`, and `country`.
4. Define public setter methods to assign values to the variables.
5. Define public getter methods to retrieve the values of the variables.
6. Create a `Scanner` object to read input from the user.
7. Read the person's name, age, and country.
8. Create an object of the `Person` class.
9. Use the setter methods to store the input values in the object.
10. Use the getter methods to retrieve and display the stored values.
11. End the program.

## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.*;
public class Person {
  
    private String name;
    private int age;
    private String country;

   
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }

    
    public int getAge() {
        return age;
    }
    public void setAge(int age) {
        this.age = age;
    }

    
    public String getCountry() {
        return country;
    }
    public void setCountry(String country) {
        this.country = country;
    }
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        String name=sc.nextLine();
        int age=sc.nextInt();
        sc.nextLine();
        String country=sc.nextLine();
        Person p=new Person();
        p.setName(name);
        p.setAge(age);
        p.setCountry(country);
        System.out.println("Person 1");
        System.out.println("Name: "+p.getName());
        System.out.println("Age: "+p.getAge());
        System.out.println("Country: "+p.getCountry());
    }
}
```

## OUTPUT:
<img width="762" height="380" alt="image" src="https://github.com/user-attachments/assets/92bdacb8-fd41-4639-bd8c-75c82acf1e10" />



## RESULT:
The program successfully demonstrates encapsulation by using private instance variables and public getter and setter methods to store and display the details of a person.
