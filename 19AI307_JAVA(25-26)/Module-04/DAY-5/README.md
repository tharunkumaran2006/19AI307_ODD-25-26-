# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create a ChatRoom class (mediator) and two users (colleagues) who send and receive messages through it. No direct communication allowed. (Mediator Pattern)

## AIM:
To write a Java program that demonstrates the Mediator Design Pattern using a `ChatRoom` class to manage communication between users without allowing direct interaction between them.

## ALGORITHM :
1. Start the program.
2. Create a `ChatRoom` class that acts as the mediator.
3. Maintain a collection of registered users in the `ChatRoom`.
4. Create a `User` class with attributes for user name and chat room reference.
5. Register each user with the `ChatRoom` when the user object is created.
6. Define a `send()` method in the `User` class to send messages through the `ChatRoom`.
7. Define a `sendMessage()` method in the `ChatRoom` to forward messages to the intended receiver.
8. Define a `receive()` method in the `User` class to display received messages.
9. Create a `Scanner` object to read input.
10. Read the names of two users and create their objects.
11. Read the number of messages to be exchanged.
12. For each message, read the sender name, receiver name, and message content.
13. Send the message through the mediator (`ChatRoom`).
14. Display the received message in the specified format.
15. End the program.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: THARUN V K
RegisterNumber:  212223230231
*/
```

## SOURCE CODE:
```java
import java.util.*;

class ChatRoom {
    private Map<String, User> users = new HashMap<>();

    public void register(User user) {
        users.put(user.getName(), user);
    }

    public void sendMessage(String from, String to, String message) {
        User receiver = users.get(to);

        if (receiver != null) {
            receiver.receive(from, message);
        }
    }
}

class User {
    private String name;
    private ChatRoom chatRoom;

    public User(String name, ChatRoom chatRoom) {
        this.name = name;
        this.chatRoom = chatRoom;
        chatRoom.register(this);
    }
    public void send(String to, String message) {
        chatRoom.sendMessage(name, to, message);
    }

    public void receive(String from, String message) {
        System.out.println(from + " to " + name + ": " + message);
    }

    public String getName() {
        return name;
    }
}

public class ChatApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        ChatRoom room = new ChatRoom();

        String user1 = sc.nextLine();
        String user2 = sc.nextLine();

        User u1 = new User(user1, room);
        User u2 = new User(user2, room);

        int n = Integer.parseInt(sc.nextLine());

        for (int i = 0; i < n; i++) {
            String sender = sc.nextLine();
            String receiver = sc.nextLine();
            String message = sc.nextLine();

            if (u1.getName().equals(sender)) {
                u1.send(receiver, message);
            } else {
                u2.send(receiver, message);
            }
        }

        sc.close();
    }
}
```

## OUTPUT:
<img width="1176" height="585" alt="image" src="https://github.com/user-attachments/assets/aa79c4f2-97e9-4a0a-993e-c2d3f9265fd5" />



## RESULT:
The program successfully demonstrates the Mediator Design Pattern by enabling communication between users through a central `ChatRoom` mediator without allowing direct communication between the users.
