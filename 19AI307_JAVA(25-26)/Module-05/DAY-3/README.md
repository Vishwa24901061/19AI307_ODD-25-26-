# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to count the number of words in a file.

## AIM:
To Write a program to count the number of words in a file.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a full line of text from the user and write it into a file using BufferedWriter.
4.	Open the same file using BufferedReader to read its contents line by line.
5.	For each line, trim it and split it into words using whitespace as the delimiter.
6.	Count all valid words and accumulate the total word count.
7.	Print the total number of words and close all streams properly.






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
import java.io.*;
import java.util.Scanner;

public class WordCountFile {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String fileName = "input.txt";

        try {
            String input = sc.nextLine();

            BufferedWriter writer = new BufferedWriter(new FileWriter(fileName));
            writer.write(input);
            writer.close();

            BufferedReader reader = new BufferedReader(new FileReader(fileName));
            int wordCount = 0;
            String line;
            while ((line = reader.readLine()) != null) {
                String[] words = line.trim().split("\\s+"); 
                if (!line.trim().isEmpty()) {
                    wordCount += words.length;
                }
            }
            reader.close();

            System.out.println("Number of words in the file: " + wordCount);

        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            sc.close();
        }
    }
}
```






## OUTPUT:
<img width="1137" height="250" alt="image" src="https://github.com/user-attachments/assets/464a8ea0-58a3-4297-a4a1-57645ed42f12" />


## RESULT:
Thus, the program to count the number of words in a file executed successfully.
