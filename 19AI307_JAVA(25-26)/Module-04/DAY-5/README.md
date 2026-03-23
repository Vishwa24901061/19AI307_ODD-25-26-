# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create a program that sends different types of notifications: "email", "sms", and "push". Use the Factory Pattern to generate the appropriate notification sender and call its notifyUser() method.

## AIM:
To write a Java program that demonstrates a Behavioral Pattern using the Factory Method, allowing different notification types to send messages through a common interface.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an interface Notification with method notifyUser().
4. Implement concrete classes: EmailNotification, SMSNotification, and PushNotification.
5. Create a NotificationFactory that returns the appropriate object based on user input.
6. In main(), get the notification type from the user.
7. Call the notifyUser() method of the returned object.
8. If no valid type is provided, display an error.
9. Stop the program.	





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: VISHWA V
RegisterNumber: 212224110062
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;

interface Notification {
    void notifyUser();
}

// ===== Concrete Notifications =====
class EmailNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Email Notification");
    }
}

class SMSNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending SMS Notification");
    }
}

class PushNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Push Notification");
    }
}

// ===== Factory =====
class NotificationFactory {
    public Notification createNotification(String type) {
        if (type == null) return null;
        switch (type.toLowerCase()) {
            case "email":
                return new EmailNotification();
            case "sms":
                return new SMSNotification();
            case "push":
                return new PushNotification();
            default:
                return null;
        }
    }
}

// ===== Main =====
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        NotificationFactory factory = new NotificationFactory();

        while (true) {
            String input = sc.nextLine().trim();
            if (input.equalsIgnoreCase("exit")) break;

            Notification n = factory.createNotification(input);
            if (n != null) {
                n.notifyUser();
            } else {
                System.out.println("Invalid notification type: " + input);
            }
        }

        sc.close();
    }
}
```





## OUTPUT:

<img width="683" height="314" alt="image" src="https://github.com/user-attachments/assets/edf5fe49-f708-4e83-be44-62fb79f933b2" />


## RESULT:
Thus, the program demonstrating the Behavioral Pattern using Factory Method to generate different notification types was successfully implemented and executed.
