# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Maintain two int variables a and b, read their initial values from user. Use synchronized block to swap them and print swapped values.

## AIM:
To write a Java program that reads two integers from the user and swaps their values using a synchronized block to ensure thread-safe operations.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Enter the synchronized block using the lock object.

Swap the values of a and b using a temporary variable.

Exit the synchronized block once the swap is complete.

Print the swapped values of a and b.

Close the scanner.





## PROGRAM:
 ```java
/*
Program to implement a Synchronization concept using Java
Developed by: JAI HARISH R
RegisterNumber: 212224040124
*/

## SOURCE CODE:

import java.util.Scanner;

public class SwapUsingSynchronized {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        Object lock = new Object();

        synchronized (lock) {
            int temp = a;
            a = b;
            b = temp;
        }

        System.out.println("a = " + a);
        System.out.println("b = " + b);
        sc.close();
    }
}
```





## OUTPUT:

<img width="516" height="438" alt="image" src="https://github.com/user-attachments/assets/c5ad1841-a051-4817-88cc-0b71efc36910" />



## RESULT:

Therefore the program successfully swaps two integers within a synchronized block, ensuring safe and controlled access.
