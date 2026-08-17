# System.Out
Imagine your Java program is a person inside a room.
* **`System`** is the room itself. It represents your computer's system.
* **`out`** is a window in that room. It is the designated "Standard Output" window where the program can throw messages out for you to see.
* **Methods like `println()`** are the specific actions of throwing the message out the window.

### Visual Breakdown Diagram

```text
  [ Your Java Program ] 
           |
           v
+-----------------------+       
|    System Class       | ---> A built-in Java class that contains useful tools.
+-----------------------+       
           |
           v
+-----------------------+       
|       .out            | ---> A static tool (object) inside the System class. 
+-----------------------+      It represents the standard screen/console.
           |
           v
+-----------------------+       
|      Methods          | ---> The actions you can perform using '.out'
+-----------------------+       
   ├── .print()         (Prints text on the same line)
   ├── .println()       (Prints text and moves to a new line)
   ├── .printf()        (Prints formatted text)
   └── .format()        (Also prints formatted text - twin of printf!)
```

---

## 2. The Four Main Methods of `System.out`

Because `out` is a special object (technically a `PrintStream` object), it has its own built-in actions called **methods**. Let's look at the four most important ones you will use.

### A. `System.out.println()` 
*(Pronounced: print-line)*

This is the most common method. It prints whatever you tell it to, and then **automatically presses "Enter"** at the end, so the next thing printed will be on a new line.

**Syntax:**
```java
System.out.println("Your message here");
```

**Example Code:**
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, buddy!");
        System.out.println("Welcome to Java.");
    }
}
```

**Output on Screen:**
```text
Hello, buddy!
Welcome to Java.
```

---

### B. `System.out.print()`

This is similar to `println()`, but it **does NOT press "Enter"** at the end. The cursor stays on the exact same line. Anything printed next will be squished right next to it.

**Syntax:**
```java
System.out.print("Your message here");
```

**Example Code:**
```java
public class PrintExample {
    public static void main(String[] args) {
        System.out.print("Learning ");
        System.out.print("Java ");
        System.out.print("is fun!");
    }
}
```

**Output on Screen:**
```text
Learning Java is fun!
```
*(Notice how it's all on one line because we used `print` instead of `println`!)*

---

### C. `System.out.printf()` 
*(Pronounced: print-format)*

Sometimes you want to inject variables (data) into a sentence cleanly. `printf()` lets you use "placeholders" to format your text beautifully. 

* `%s` is a placeholder for a String (text).
* `%d` is a placeholder for a digit (whole number).
* `%n` means new line.

**Syntax:**
```java
System.out.printf("Text with placeholders", variable1, variable2);
```

**Example Code:**
```java
public class FormatExample {
    public static void main(String[] args) {
        String language = "Java";
        int version = 21;
        
        System.out.printf("I am learning %s version %d.%n", language, version);
    }
}
```

**Output on Screen:**
```text
I am learning Java version 21.
```

---

### D. `System.out.format()` 
*(The Twin Brother of printf!)*

Great catch noticing this one! `format()` and `printf()` are **exactly the same thing** in Java. Under the hood, `printf()` actually just calls `format()`. Java included both because `printf()` is familiar to developers coming from the 'C' programming language, while `format()` fits standard Java naming conventions.

**Syntax:**
```java
System.out.format("Text with placeholders", variable1, variable2);
```

**Example Code:**
```java
public class FormatMethodExample {
    public static void main(String[] args) {
        String item = "Coffee";
        double price = 2.50;
        
        // %.2f formats a decimal number to 2 decimal places
        System.out.format("One %s costs $%.2f.%n", item, price);
    }
}
```

**Output on Screen:**
```text
One Coffee costs $2.50.
```

---

## 3. Related Topics (Expanding Your Knowledge)

Since you are learning about `System.out`, you should also know about its two siblings! They all live inside the `System` class.

### 1. `System.in` (Standard Input)
If `System.out` is the window to throw messages *out*, `System.in` is the door to bring messages *in*. We use it to read data typed by the user on the keyboard. 
*(We usually wrap it in a `Scanner` tool to make reading easier).*

**Example Snippet:**
```java
import java.util.Scanner;

Scanner input = new Scanner(System.in); // Reading from the keyboard
```

### 2. `System.err` (Standard Error)
This works exactly like `System.out.println()`, but it is meant specifically for printing **error messages**. In many modern code editors, using `System.err.println("Error!");` will print the text in **Red color** to grab your attention.

**Example Snippet:**
```java
System.err.println("File not found!"); // Prints like an error
```

---

## Summary Cheat Sheet

| Command | What it does | When to use it? |
|---------|--------------|-----------------|
| `System.out.println()` | Prints text + goes to the next line. | 90% of the time. Easiest way to display info. |
| `System.out.print()` | Prints text + stays on the same line. | When you want to combine multiple print statements into one line. |
| `System.out.printf()` | Prints text with special formatting placeholders. | When inserting multiple variables into a sentence perfectly. |
| `System.out.format()` | **Identical to `printf()`.** | Whenever you prefer the word "format" over "printf"! |

* ##  Format Specifier☕

Imagine you have a fill-in-the-blank sentence: 
> "Hello, my name is ____ and I am ____ years old."

In Java, when we want to print sentences with variables, we use a special method called `printf` (which stands for "print formatted"). 

A **Format Specifier** is simply the "blank space" in your code. It tells Java: *"Hey, hold this spot! I'm going to put a specific type of data (like a word or a number) here in a moment."*

All format specifiers in Java start with the percentage sign: `%`

### Visual Analogy:
```text
System.out.printf("Hello, my name is %s and I am %d years old.", "Alice", 25);
                                     |                 |           |      |
                                     V                 V           |      |
                                  (Blank 1)         (Blank 2)      |      |
                                     |                 |           |      |
                                     +-----------------------------+      |
                                                       |                  |
                                                       +------------------+
```
*(Here, `%s` grabs "Alice", and `%d` grabs 25!)*

---

## 2. Where Do We Use Them? 🛠️

Format specifiers are mostly used with two commands in Java:
1. `System.out.printf()` - Used to print formatted text directly to the screen.
2. `String.format()` - Used to save formatted text into a String variable to use later.

---

## 3. The Most Common Format Specifiers 📋

Here is a cheat sheet of the ones you will use 99% of the time. Think of the letter after the `%` as a clue to what data it holds!

| Specifier | Stands For | Data Type it accepts | Example Output |
| :---: | :--- | :--- | :--- |
| **`%d`** | **D**ecimal Integer | `int`, `long`, `short`, `byte` | `42` |
| **`%f`** | **F**loating-point | `float`, `double` | `3.141590` |
| **`%s`** | **S**tring | `String` | `"Hello"` |
| **`%c`** | **C**haracter | `char` | `'A'` |
| **`%b`** | **B**oolean | `boolean` | `true` or `false` |
| **`%n`** | **N**ew line | (None, just breaks to next line) | *Moves to next line* |

---

## 4. The Anatomy of a Format Specifier 🔬

Format specifiers can do more than just hold a place. They can also control **how** the data looks (like adding spaces or rounding numbers). 

Here is the secret formula (everything in brackets `[]` is optional):

```text
% [flags] [width] [.precision] conversion-character
```

### Visual Breakdown:
```text
Example:  %05.2f

  %      0       5       .2       f
  |      |       |       |        |
  |      |       |       |        +--> Conversion: It's a float/double number.
  |      |       |       +-----------> Precision: Show exactly 2 decimal places.
  |      |       +-------------------> Width: The whole output must take up 5 spaces.
  |      +---------------------------> Flag: Fill empty spaces with zeros instead of blanks.
  +----------------------------------> Start: Every specifier starts with %
```

### Let's look at what each part does:

#### A. Width (Adding Spaces)
You can tell Java how many characters of space a value should take up. This is amazing for aligning tables!
* `"%5d"` applied to the number `9` will output `"    9"` (4 spaces + the number 9 = 5 characters wide).

#### B. Precision (Rounding Decimals)
Used mostly with `%f` (floating-point numbers) to limit decimal places.
* `"%.2f"` applied to `3.14159` will output `"3.14"`.

#### C. Flags (Aligning and Padding)
* `-` (Minus sign): Left-aligns the text (e.g., `"%-5d"`). By default, Java right-aligns.
* `0` (Zero): Pads with zeros instead of spaces (e.g., `"%05d"` applied to `9` becomes `"00009"`).
* `,` (Comma): Adds grouping separators for large numbers (e.g., `"%,d"` applied to `1000000` becomes `"1,000,000"`).

---

## 5. Complete Example Code 💻

Here is a simple Java program that puts everything together. You can copy and paste this into your IDE (like IntelliJ, Eclipse, or VS Code) to run it!

```java
public class FormattingMagic {
    public static void main(String[] args) {
        
        // 1. Basic Variables
        String name = "Jack";
        int age = 28;
        double balance = 1250.509;
        
        // --- Examples ---
        
        // Example 1: Basic string and integer insertion
        System.out.printf("Name: %s, Age: %d %n", name, age);
        // Output: Name: Jack, Age: 28 
        
        // Example 2: Precision with floating numbers (Rounding to 2 decimals)
        System.out.printf("Bank Balance: $%.2f %n", balance);
        // Output: Bank Balance: $1250.51
        
        // Example 3: Width & Flags (Making neat columns)
        System.out.println("--- Store Inventory ---");
        System.out.printf("%-10s | %-5s %n", "ITEM", "PRICE");  // Left-aligned
        System.out.printf("%-10s | $%.2f %n", "Apple", 1.25);
        System.out.printf("%-10s | $%.2f %n", "Watermelon", 5.00);
        
        // Example 4: Zero padding (Great for IDs or time!)
        int employeeId = 42;
        System.out.printf("Your Employee ID is: %05d %n", employeeId);
        // Output: Your Employee ID is: 00042
    }
}
```

---

### A. Escape Sequences vs `%n`
You might see people use `
` to create a new line in Java. While `
` works inside regular `print()` or `println()`, it is best practice to use `%n` inside `printf()`. 
* **Why?** Because `%n` automatically figures out the correct new-line character for whatever operating system you are running on (Windows uses `
`, Mac/Linux uses `
`).

### B. The `Scanner` Class (Reading Input)
Right now, you are outputting formatted data. Soon, you'll want to *take in* data from the user. You will use the `Scanner` class for this. Interestingly, Scanner uses methods that match these data types:
* `%d` (integer) pairs nicely with `scanner.nextInt()`
* `%f` (double) pairs nicely with `scanner.nextDouble()`
* `%s` (String) pairs nicely with `scanner.next()`

---