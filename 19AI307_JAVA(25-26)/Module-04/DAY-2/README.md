# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
You are designing a microservices-based system where multiple services like AuthService, UserService, OrderService, etc., need to log important system events.

To maintain centralized logging (and not have separate loggers for each service), the system uses a Singleton Logger.

Each service logs messages with its name and log level.

Log levels can be: INFO, WARNING, or ERROR.

Every log message is stored in order of occurrence and the logger prints the entire log history each time a new message is added.

🧩 Concepts Student Must Apply:
Implement a Singleton class (Logger) that holds logs.

Maintain logs as a list of strings.

Each log message must be formatted as:
"[Service] [LEVEL]: message"

Print full log history after each new log.

## AIM:
To write a Java program that implements the Singleton design pattern for centralized logging, stores log messages in a list, and displays the complete log history whenever a new log is added.

## ALGORITHM :
1. Start the program.
2. Create a `Logger` class following the Singleton design pattern.
3. Declare a private static instance of the `Logger` class.
4. Create a private constructor to prevent direct object creation.
5. Maintain a list to store all log messages.
6. Define a `getInstance()` method to return the single `Logger` instance.
7. Define an `addLog()` method to:

   * Format the log message using the service name, log level, and message.
   * Store the log in the list.
   * Display the newly added log.
   * Print the complete log history.
8. In the main method, read the number of log entries.
9. For each log entry, read the service name, log level, and message.
10. Obtain the Singleton `Logger` instance using `getInstance()`.
11. Add the log entry using the `addLog()` method.
12. Repeat until all log entries are processed.
13. End the program.

## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.*;

class Logger {

    private static Logger instance;
    private List<String> logs;

    private Logger() {
        logs = new ArrayList<>();
    }

    public static Logger getInstance() {
        if (instance == null) {
            instance = new Logger();
        }
        return instance;
    }

    public void addLog(String service, String level, String message) {
        String log = service + " " + level + ": " + message;

        logs.add(log);

        System.out.println(log);
        System.out.println("Current Logs:");

        for (int i = 0; i < logs.size(); i++) {
            System.out.println((i + 1) + ". " + logs.get(i));
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String[] input = sc.nextLine().split(" ");

            String service = input[0];
            String level = input[1];
            String message = input[2];

            Logger logger = Logger.getInstance();
            logger.addLog(service, level, message);

            System.out.println();
        }

        sc.close();
    }
}
```

## OUTPUT:
<img width="985" height="540" alt="image" src="https://github.com/user-attachments/assets/024b5f2a-5d10-4693-bfa6-7fbf616245a5" />



## RESULT:
The program successfully implements a Singleton Logger that maintains a centralized log history, stores all log messages in order of occurrence, and displays the complete log history whenever a new log entry is added.
