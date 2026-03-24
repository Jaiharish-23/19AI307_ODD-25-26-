# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a Java program to create a new file named example.txt.

## AIM:

To write a Java program that creates a new file named example.txt using the File class and handles any possible I/O exceptions.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	If the method returns true, print that the file was created.

If it returns false, print that the file already exists.

Surround the file-creation logic with a try–catch block to handle IOException.





## PROGRAM:
 ```java
/*
Program to implement a File Handling using Java
Developed by: JAI HARISH R
RegisterNumber: 212224040124
*/

## SOURCE CODE:

import java.io.File;
import java.io.IOException;

public class CreateNewFileExample {
    public static void main(String[] args) {
        try {
            File file = new File("example.txt");
            if (file.createNewFile()) {
                System.out.println("File created: " + file.getName());
            } else {
                System.out.println("File already exists.");
            }
        } catch (IOException e) {
            System.out.println("An error occurred: " + e.getMessage());
        }
    }
}
```




## OUTPUT:

<img width="870" height="296" alt="image" src="https://github.com/user-attachments/assets/c6cf4238-8ad9-4869-b129-e25e19646077" />


## RESULT:

Therefore the program successfully creates a new file named example.txt if it does not already exist.
