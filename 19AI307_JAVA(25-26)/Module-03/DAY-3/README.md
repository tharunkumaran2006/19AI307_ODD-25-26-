# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create abstract class GameScore with method finalScore().
Subclasses:

ArcadeGame: score = baseScore + (level × 100)

PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

## AIM:
To write a Java program using an abstract class `GameScore` and its subclasses `ArcadeGame` and `PuzzleGame` to calculate and display the final game score based on different scoring rules.

## ALGORITHM :
1. Start the program.
2. Create an abstract class `GameScore` with an abstract method `finalScore()`.
3. Create a subclass `ArcadeGame` with attributes `baseScore` and `level`.
4. Override the `finalScore()` method to calculate the score as `baseScore + (level × 100)`.
5. Create a subclass `PuzzleGame` with the attribute `attempts`.
6. Override the `finalScore()` method:

   * If `attempts ≤ 3`, calculate the score as `1000 - (attempts × 100)`.
   * Otherwise, return `500`.
7. Create a `Scanner` object to read input.
8. Read the game type from the user.
9. If the game type is `1`, read `baseScore` and `level` and create an `ArcadeGame` object.
10. Otherwise, read `attempts` and create a `PuzzleGame` object.
11. Call the `finalScore()` method using the object.
12. Display the calculated final score.
13. End the program.






## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

abstract class GameScore {
    abstract int finalScore();
}
class ArcadeGame extends GameScore {

    int baseScore;
    int level;

    ArcadeGame(int baseScore, int level) {
        this.baseScore = baseScore;
        this.level = level;
    }
    int finalScore() {
        return baseScore + (level * 100);
    }
}

class PuzzleGame extends GameScore {

    int attempts;

    PuzzleGame(int attempts) {
        this.attempts = attempts;
    }
    int finalScore() {

        if (attempts <= 3) {
            return 1000 - (attempts * 100);
        } else {
            return 500;
        }
    }
}

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int type = sc.nextInt();

        GameScore game;

        if (type == 1) {

            int base = sc.nextInt();
            int level = sc.nextInt();

            game = new ArcadeGame(base, level);

        } else {

            int attempts = sc.nextInt();

            game = new PuzzleGame(attempts);
        }

        System.out.println(game.finalScore());

        sc.close();
    }
}
```


## OUTPUT:
<img width="533" height="161" alt="image" src="https://github.com/user-attachments/assets/f60dd872-58b9-4581-bc9d-1be39f9d4c5d" />



## RESULT:
The program successfully demonstrates abstraction by using an abstract class and calculates the final score for Arcade and Puzzle games according to their respective scoring rules.
