# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is prime using wrapper classes.

## AIM:

To write a Java program that checks whether a given number is prime by using the Integer wrapper class for parsing and handling the input.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.If parsing fails, catch NumberFormatException and display an error message.

If the number is less than or equal to 1, it is not prime.

If any divisor divides the number completely, mark it as not prime.

After checking, print whether the number is prime or not.

Close the scanner.	





## PROGRAM:
 ```java
/*
Program to implement a Wrapper Class using Java
Developed by: JAI HARISH R
RegisterNumber: 212224040124
*/

## SOURCE CODE:


import java.util.Scanner;

public class PrimeChecker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        
        String input = scanner.nextLine();

        try {
            Integer number = Integer.parseInt(input); // Using Integer wrapper class

            if (number <= 1) {
                System.out.println(number + " is not a prime number.");
            } else {
                boolean isPrime = true;
                for (int i = 2; i <= Math.sqrt(number); i++) {
                    if (number % i == 0) {
                        isPrime = false;
                        break;
                    }
                }

                if (isPrime) {
                    System.out.println(number + " is a prime number.");
                } else {
                    System.out.println(number + " is not a prime number.");
                }
            }

        } catch (NumberFormatException e) {
            System.out.println("Invalid input. Please enter a valid integer.");
        }

        scanner.close();
    }
}
```




## OUTPUT:

<img width="1003" height="293" alt="image" src="https://github.com/user-attachments/assets/59974151-7432-4cd6-b456-f96c579d75dc" />


## RESULT:

Therefore the program successfully checks if the input number is a prime using the Integer wrapper class.
