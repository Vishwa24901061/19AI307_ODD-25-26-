# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase. However, you're getting a NullPointerException. What should you check in your array before calling .toUpperCase() on a element?

## AIM:
To handle a NullPointerException when performing operations on a null string in Java.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a string input from the user.
4.	If the input is "null", assign null to the variable.
5.	Try converting the string to uppercase using toUpperCase().
6.	Catch and handle the NullPointerException if the string is null.
7.	Print "Null element" in case of exception.





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

public class NullPointerArrayExample {
   public static void main(String[] args) {
       Scanner sc = new Scanner(System.in);

       String input = sc.next();
       String str = input.equalsIgnoreCase("null") ? null : input;

       try {
           System.out.println(str.toUpperCase());
       } catch (NullPointerException e) {
           System.out.println("Null element");
       }

       sc.close();
   }
}

```




## OUTPUT:
<img width="1113" height="211" alt="image" src="https://github.com/user-attachments/assets/0f95d882-b70a-434c-b780-6fb87786107e" />



## RESULT:
The program successfully detects and handles NullPointerException by displaying "Null element" when the input is null.
