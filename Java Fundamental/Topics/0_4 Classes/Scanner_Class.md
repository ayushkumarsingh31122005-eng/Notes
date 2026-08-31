* # Java has some Inbuild classes int's Librabry.
# 1. What is the Scanner Class?

The `Scanner` class is a built-in feature in Java used to read input from various sources like the keyboard, files, or even strings. For beginners, we mostly use it to read input from the **keyboard**.

It is located in the `java.util` package. A package is simply a folder where related Java features are stored. Because it's in a separate folder, we have to **import** it before we can use it.

### Syntax to Import:
```java
import java.util.Scanner;
```

---

## 2. How to Create a Scanner Object

Before you can use the `Scanner`, you must create an "object" (an instance) of it. 

### Syntax:
```java
Scanner myScanner = new Scanner(System.in);
```

**Let's break this down:**
*   `Scanner`: The type of object we are making.
*   `myScanner`: The name we are giving to our scanner (you can name it `input`, `sc`, or anything you like!).
*   `new Scanner(...)`: This creates the actual object in the computer's memory.
*   `System.in`: This tells the Scanner *where* to listen for input. `System.in` means "Standard Input," which is your keyboard!

---

## 3. Important Methods of the Scanner Class

A **method** is simply an action that an object can perform. Depending on what kind of data you want from the user (a number, a word, a sentence), you use a different method.

Here is a visual cheat sheet of the most important methods:

| Method | What it reads | Example Input | Java Data Type |
| :--- | :--- | :--- | :--- |
| **`nextLine()`** | Reads a **complete line** of text (until you press Enter). | "John Doe" | `String` |
| **`next()`** | Reads a **single word** (stops at the first space). | "John" | `String` |
| **`nextInt()`** | Reads an **integer** (whole number). | `25` | `int` |
| **`nextDouble()`** | Reads a **decimal number**. | `19.99` | `double` |
| **`nextBoolean()`**| Reads a **true or false** value. | `true` | `boolean` |
| **`close()`** | Closes the scanner to save computer memory. | N/A | N/A |

---

## 4. Complete Code Example

Let's put it all together in a real Java program. You can copy and paste this into your IDE (like IntelliJ, Eclipse, or VS Code) to run it!

```java
import java.util.Scanner; // Step 1: Import the Scanner class

public class Main {
    public static void main(String[] args) {
        
        // Step 2: Create a Scanner object to read from the keyboard
        Scanner sc = new Scanner(System.in);

        // --- Example 1: Reading a String (Whole line) ---
        System.out.print("Enter your full name: ");
        String name = sc.nextLine(); 

        // --- Example 2: Reading an Integer ---
        System.out.print("Enter your age: ");
        int age = sc.nextInt();

        // --- Example 3: Reading a Double (Decimal) ---
        System.out.print("Enter your exact height in meters (e.g., 1.75): ");
        double height = sc.nextDouble();

        // --- Example 4: Reading a Boolean ---
        System.out.print("Do you love programming? (true/false): ");
        boolean lovesCoding = sc.nextBoolean();

        // Step 3: Print out the collected information
        System.out.println("\n--- User Profile ---");
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Height: " + height + "m");
        System.out.println("Loves Coding: " + lovesCoding);

        // Step 4: Close the scanner! (Good practice)
        sc.close();
    }
}
```

---

####  The Scanner class in Java does not have a built-in nextChar() method. To read a single character from the user, you must read the input as a string first using next() or nextLine(), and then extract its first character using charAt(0).

 * **syntax**
 ```
 char ch = scanner.next().charAt(0);
 ```

