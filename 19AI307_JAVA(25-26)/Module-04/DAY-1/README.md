# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase. However, you're getting a NullPointerException. What should you check in your array before calling .toUpperCase() on a element?

## AIM:
To write a Java program that demonstrates a NullPointerException when calling .toUpperCase() on a null string, and to show how to handle it safely.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Use a try block to call str.toUpperCase().

If str is null, a NullPointerException will occur and be caught in the catch block.

Print "Null element" when the exception is caught.

Close the scanner.





## PROGRAM:
 ```java
/*
Program to implement a Exception Handling using Java
Developed by: JAI HARISH R
RegisterNumber: 212224040124
*/

## SOURCE CODE:

import java.util.Scanner;

public class NullPointerArrayExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String input = sc.nextLine();
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
<img width="712" height="415" alt="image" src="https://github.com/user-attachments/assets/0bfcae96-f5b2-4261-9365-d95fe798e810" />



## RESULT:

Therefore the program successfully demonstrates how a NullPointerException occurs when calling .toUpperCase() on a null value.
