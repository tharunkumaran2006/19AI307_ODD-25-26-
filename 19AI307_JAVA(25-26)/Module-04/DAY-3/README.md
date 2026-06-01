# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Create animals from two regions: "Africa" and "Asia". Use Abstract Factory to create families of animals (Herbivore, Carnivore). Print the interaction result.

## AIM:
To write a Java program that demonstrates the Abstract Factory Design Pattern by creating related families of animals (Herbivore and Carnivore) for different regions and displaying their interaction.

## ALGORITHM :
1. Read the region name from the user.
2. Create interfaces `Herbivore` and `Carnivore`.
3. Define the method `eat()` in the `Carnivore` interface.
4. Create animal classes for Africa (`Wildebeest`, `Lion`) and Asia (`Buffalo`, `Tiger`).
5. Create an `AnimalFactory` interface with methods to create herbivores and carnivores.
6. Implement `AfricaFactory` and `AsiaFactory` to create the corresponding animal families.
7. Based on the input region, create the appropriate factory object.
8. If the region is invalid, display an error message and terminate the program.
9. Use the factory to create a herbivore and a carnivore.
10. Invoke the `eat()` method of the carnivore, passing the herbivore as an argument.
11. Display the interaction result.
12. End the program.




## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

interface Herbivore {}
interface Carnivore {
    void eat(Herbivore h);
}

class Wildebeest implements Herbivore {}
class Lion implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Lion eats Wildebeest");
    }
}

class Buffalo implements Herbivore {}
class Tiger implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Tiger eats Buffalo");
    }
}

interface AnimalFactory {
    Herbivore createHerbivore();
    Carnivore createCarnivore();
}

class AfricaFactory implements AnimalFactory {
    public Herbivore createHerbivore() { return new Wildebeest(); }
    public Carnivore createCarnivore() { return new Lion(); }
}

class AsiaFactory implements AnimalFactory {
    public Herbivore createHerbivore() { return new Buffalo(); }
    public Carnivore createCarnivore() { return new Tiger(); }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String region = sc.nextLine().toLowerCase();
        AnimalFactory factory;

        if (region.equals("africa")) factory = new AfricaFactory();
        else if (region.equals("asia")) factory = new AsiaFactory();
        else {
            System.out.println("Invalid region");
            return;
        }

        Carnivore carn = factory.createCarnivore();
        Herbivore herb = factory.createHerbivore();
        carn.eat(herb);
    }
}

```

## OUTPUT:
<img width="596" height="174" alt="image" src="https://github.com/user-attachments/assets/b1e29324-03ea-421e-8f3f-6635ffb93c1f" />



## RESULT:
The program successfully demonstrates the Abstract Factory Design Pattern by creating region-specific families of animals and displaying the interaction between the carnivore and herbivore.
