# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to demonstrate chaining of streams (BufferedReader on top of InputStreamReader on top of System.in)

## AIM:
To Write a program to demonstrate chaining of streams (BufferedReader on top of InputStreamReader on top of System.in)

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a BufferedReader object chained with InputStreamReader to read input from the keyboard.
4.	Read the user’s name as a string using readLine().
5.	Read the age as a string, then convert it to an integer using Integer.parseInt().
6.	Display the user details (name and age) on the screen.
7.	Close the BufferedReader and handle any possible IOException.	






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
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class ChainingStreamsExample {
    public static void main(String[] args) {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        try {
            String name = br.readLine(); 

            String ageInput = br.readLine(); 
            int age = Integer.parseInt(ageInput); 

            System.out.println("--- User Details ---");
            System.out.println("Name: " + name);
            System.out.println("Age: " + age);

            br.close();
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```






## OUTPUT:
<img width="701" height="402" alt="image" src="https://github.com/user-attachments/assets/234259fe-b2de-4385-b85f-cb8c70a525f5" />



## RESULT:
Thus, the program to demonstrate chaining of streams is executed successfully.
