# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class City with attributes: cityName (String), population (long), area (double). Create an object. Print all details.

## AIM:
To create a Java class `City` with the attributes `cityName`, `population`, and `area`, create an object of the class, and display all the city details.

### ALGORITHM
1. Start the program.
2. Import the package `java.util`.
3. Create a class `City` with attributes `cityName`, `population`, and `area`.
4. Define a method `printDetails()` to display the city details.
5. Create the main class and define the `main()` method.
6. Create a `Scanner` object to read input from the user.
7. Create an object of the `City` class.
8. Read the city name, population, and area from the user and store them in the object's attributes.
9. Call the `printDetails()` method using the object.
10. Display the city details.
11. Close the scanner.
12. End the program.

## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;
class City {

    String cityName;
    long population;
    double area;

    void printDetails() {
        System.out.println("City Name: "+cityName);
        System.out.println("Population: "+population);
        System.out.println("Area: "+area);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        City c=new City();
        c.cityName=sc.nextLine();
        c.population=sc.nextInt();
        c.area=sc.nextDouble();
        c.printDetails();
        sc.close();
    }
}
```


## OUTPUT:
<img width="500" height="309" alt="image" src="https://github.com/user-attachments/assets/fbf53318-0a25-41b9-876d-836dd2dd0ab5" />



## RESULT:
The program successfully creates a `City` object, stores the city name, population, and area, and displays all the city details.
