# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:

Create a ChatRoom class (mediator) and two users (colleagues) who send and receive messages through it. No direct communication allowed.
## AIM:

Implement the Mediator pattern using a ChatRoom class to manage communication between User objects, preventing direct interaction.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read two user names and create User objects, automatically registering them with the chat room.

Read the number of chat exchanges.

For each exchange read sender, receiver, and message, call the corresponding user’s send() method.

Ensure all communication happens only through the mediator (ChatRoom), not directly between users.





## PROGRAM:
 ```java
/*
Program to implement a Behaviour Pattern using Java
Developed by: JAI HARISH R
RegisterNumber: 212224040124
*/

## SOURCE CODE:

import java.util.*;

class ChatRoom {
    private Map<String, User> users = new HashMap<>();

    public void registerUser(User user) {
        users.put(user.getName(), user);
    }

    public void sendMessage(String from, String to, String message) {
        User receiver = users.get(to);
        if (receiver != null) {
            receiver.receive(from, message);
        } else {
            System.out.println("User " + to + " not found");
        }
    }
}

class User {
    private String name;
    private ChatRoom chatRoom;

    public User(String name, ChatRoom chatRoom) {
        this.name = name;
        this.chatRoom = chatRoom;
        chatRoom.registerUser(this);
    }

    public String getName() {
        return name;
    }

    public void send(String to, String message) {
        chatRoom.sendMessage(name, to, message);
    }

    public void receive(String from, String message) {
        System.out.println(from + " to " + name + ": " + message);
    }
}

public class ChatApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        ChatRoom room = new ChatRoom();
        User user1 = new User(sc.nextLine(), room); 
        User user2 = new User(sc.nextLine(), room);

        int n = Integer.parseInt(sc.nextLine());
        for (int i = 0; i < n; i++) {
            String sender = sc.nextLine();
            String receiver = sc.nextLine();
            String message = sc.nextLine();

            if (sender.equals(user1.getName())) {
                user1.send(receiver, message);
            } else if (sender.equals(user2.getName())) {
                user2.send(receiver, message);
            } else {
                System.out.println("Unknown sender");
            }
        }

        sc.close();
    }
}
```




## OUTPUT:

<img width="1140" height="771" alt="image" src="https://github.com/user-attachments/assets/0869de7f-b297-4a2e-b0af-c44cff7143b2" />


## RESULT:

Therefore the program successfully demonstrates message exchange using the Mediator Pattern, with all user communication routed through the ChatRoom.
