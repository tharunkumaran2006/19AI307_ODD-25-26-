# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.


 Bot Types:

SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".

RainBot: Predicts "COLD" if temperature < 20, else "WARM".

## AIM:
To write a Java program that uses an interface `WeatherBot` and its implementing classes `SunBot` and `RainBot` to predict weather conditions based on temperature.

## ALGORITHM :
1. Start the program.
2. Create an interface `WeatherBot` with a method `predict(int temperature)`.
3. Create a class `SunBot` that implements the `WeatherBot` interface.
4. In `SunBot`, return **"HOT"** if the temperature is greater than 30; otherwise return **"MODERATE"**.
5. Create a class `RainBot` that implements the `WeatherBot` interface.
6. In `RainBot`, return **"COLD"** if the temperature is less than 20; otherwise return **"WARM"**.
7. Create a `Scanner` object to read input.
8. Read the temperature and bot type from the user.
9. Create an object of `SunBot` if the bot type is 1; otherwise create an object of `RainBot`.
10. Call the `predict()` method using the object.
11. Display the prediction returned by the method.
12. End the program.

## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

interface WeatherBot {
    String predict(int temperature);
}

class SunBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature > 30) {
            return "HOT";
        } else {
            return "MODERATE";
        }
    }
}

class RainBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature < 20) {
            return "COLD";
        } else {
            return "WARM";
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int temperature = sc.nextInt();
        int botType = sc.nextInt();

        WeatherBot bot;

        if (botType == 1) {
            bot = new SunBot();
        } else {
            bot = new RainBot();
        }

        System.out.println(bot.predict(temperature));
    }
}
```

## OUTPUT:
<img width="445" height="120" alt="image" src="https://github.com/user-attachments/assets/d4b1b3c1-a947-40b1-9caa-26b2806216b8" />


## RESULT:
The program successfully demonstrates the use of interfaces by implementing different weather prediction behaviors in SunBot and RainBot and displays the appropriate prediction based on the temperature and selected bot type.
