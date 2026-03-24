# Ex.No:5(D) THREAD PRIORITY

## QUESTION:

Write a Java program to implement a extending thread class
## AIM:
To write a Java program that demonstrates multithreading by creating a user-defined thread class that extends Thread and executes its own run() method.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	In the main() method: Print a message indicating the main thread execution.

Create an instance of MyThread.

Call the start() method to begin execution in a separate thread.

Allow the thread to run independently from the main thread.






## PROGRAM:
 ```java
/*
Program to implement a Thread Priority Concept using Java
Developed by: JAI HARISH R
RegisterNumber: 212224040124
*/

## SOURCE CODE:

public class MyThread extends Thread {
    public void run() {
        for (int i = 1; i <= 5; i++) {
            System.out.println("Thread: " + i);
        }
       
    }

    public static void main(String[] args) {
        System.out.println("Main thread finished");
        MyThread t = new MyThread();
        t.start();
    }
}
```





## OUTPUT:

<img width="675" height="398" alt="image" src="https://github.com/user-attachments/assets/28336b25-ff4f-43d9-a592-f1aaa4778732" />


## RESULT:

Therefore the program successfully creates a separate thread by extending Thread and executes the overridden run() method.
