# Operator
## 1️⃣ What is an Operator?

Think of an operator as a special symbol that tells the computer to perform a specific mathematical or logical task. 
For example, in simple math: `5 + 3`, the `+` is the operator. The numbers `5` and `3` are called **operands**.

---

## 2️⃣ Arithmetic Operators in Java

Java uses these basic operators to perform everyday math. 

| Operator | Name | What it does | Example | Result |
| :---: | :--- | :--- | :--- | :--- |
| `+` | **Addition** | Adds two values together | `5 + 3` | `8` |
| `-` | **Subtraction** | Subtracts one value from another | `10 - 4` | `6` |
| `*` | **Multiplication**| Multiplies two values | `4 * 3` | `12` |
| `/` | **Division** | Divides one value by another | `10 / 2` | `5` |
| `%` | **Modulo** | Gives the **remainder** of a division | `10 % 3` | `1` (Because 10/3 is 3 with remainder 1) |

### 💻 Code Example: Arithmetic Operators
```java
public class ArithmeticDemo {
    public static void main(String[] args) {
        int a = 10;
        int b = 3;

        System.out.println("Addition: " + (a + b));       // Output: 13
        System.out.println("Subtraction: " + (a - b));    // Output: 7
        System.out.println("Multiplication: " + (a * b)); // Output: 30
        System.out.println("Division: " + (a / b));       // Output: 3 (Note: decimal is dropped for integers!)
        System.out.println("Modulo: " + (a % b));         // Output: 1
    }
}
```

---

## 3️⃣ What is an Expression?

An **expression** is simply a combination of variables, numbers (literals), and operators that produces a single final value.

*   `x + 5` is an expression.
*   `(a * b) / c` is an expression.

---

## 4️⃣ Precedence Order (BODMAS for Java)

When you have a long expression like `5 + 10 * 2`, which part does Java calculate first? Does it do `5 + 10` first, or `10 * 2` first? 

Java follows strict rules called **Operator Precedence** (just like BODMAS or PEMDAS in math).

### 🥇 The Priority List (Highest to Lowest)
1.  **Parentheses `( )`**: Highest priority! Always do what's inside brackets first.
2.  **Multiplication, Division, Modulo `*`, `/`, `%`**: These share the same priority.
3.  **Addition, Subtraction `+`, `-`**: Lowest priority.

*Note: If operators have the **same priority** (like `*` and `/`), Java reads them from **Left to Right** (this is called Associativity).*

### 🧠 Let's evaluate an expression together:
**Expression:** `int result = 5 + 10 * 2;`
1. Multiplication `*` has higher priority than Addition `+`.
2. First: `10 * 2` becomes `20`.
3. Second: `5 + 20` becomes `25`.
**Final Result:** `25`

**Expression with Parentheses:** `int result2 = (5 + 10) * 2;`
1. Brackets `()` have the highest priority.
2. First: `5 + 10` becomes `15`.
3. Second: `15 * 2` becomes `30`.
**Final Result:** `30`

---

## 5️⃣ Expressions of Different Data Types & Coercion

What happens when you mix different types of data? For example, adding an `int` (whole number) and a `double` (decimal number)?

Java uses something called **Coercion** (also known as **Type Promotion** or **Implicit Type Casting**). 

**The Golden Rule:** Java always wants to prevent data loss. So, it automatically upgrades (promotes) the smaller data type into the larger data type before doing the math!

### 🚦 The Promotion Visual:
Imagine a small box fitting into a bigger box.
`byte` ➡️ `short` ➡️ `int` ➡️ `long` ➡️ `float` ➡️ `double`

*   If you multiply an `int` by a `double`, Java temporarily turns the `int` into a `double`, and the final answer is a `double`.
*   **Special Rule for whole numbers:** In Java, if you do math with `byte`, `short`, or `char`, Java *automatically* promotes them to `int` before calculating.

### 💻 Code Example: Coercion in Action
```java
public class CoercionDemo {
    public static void main(String[] args) {
        int myInt = 5;
        double myDouble = 2.5;
        
        // myInt is automatically promoted to double (5.0) before addition
        double result = myInt + myDouble; 
        
        System.out.println("Result is: " + result); // Output: 7.5
        
        // Important Note on Division!
        int x = 5;
        int y = 2;
        System.out.println("Integer math: " + (x / y)); 
        // Output is 2! (Because int/int = int. The decimal .5 is thrown away)
        
        // How to fix integer division using Coercion? Make one a double!
        System.out.println("Double math: " + ((double)x / y)); 
        // Output is 2.5! (Here, we force x to be 5.0. Then 5.0 / 2 = 2.5)
    }
}
```

### 🔁 Explicit Casting (Manual Coercion)
Sometimes, you want to go backward (from a big box to a small box). Java won't do this automatically because you might lose data (like losing decimal points). You have to do it manually by putting the target type in parentheses. This is called **Explicit Casting**.

```java
double price = 9.99;
int roundedPrice = (int) price; // We are forcing a double into an int

System.out.println(roundedPrice); // Output: 9 (The .99 is completely chopped off!)
```
## 🌟 What is Implicit Casting?
**Implicit Casting** (also known as **Widening Casting**) happens **automatically** when you convert a smaller data type into a larger data type.

## 📊 The Rule of Implicit Casting (Visual Map)

Implicit casting only works when you go from left to right in this flow:

```text
  [SMALLEST]                                                       [LARGEST]
    byte  ➔  short  ➔  char  ➔  int  ➔  long  ➔  float  ➔  double
```
*Note: You can safely move a value from any type on the left to any type on the right.*

---
## 💻 Syntax and Code Example

Here is a simple Java program to show you how implicit casting works in action.

```java
public class ImplicitCastingExample {
    public static void main(String[] args) {
        
        // Step 1: We create a small container (int) and put the number 100 in it.
        int myInt = 100;
        
        // Step 2: We pour the 'int' into a larger container (double).
        // Java does this AUTOMATICALLY! You don't need any special syntax.
        double myDouble = myInt; 
        
        // Step 3: Let's print them out to see what happened.
        System.out.println("Original int value: " + myInt);      // Output: 100
        System.out.println("Converted double value: " + myDouble); // Output: 100.0
        
        /* 
           Notice that Java automatically added ".0" at the end because 
           'double' is used to store decimal numbers. We didn't lose any data!
        */
    }
}
```

---
---

# ⚡ How to Calculate Power (Exponents) in Java

Unlike some other programming languages (like Python, which uses `**`), Java doesn't have a specific symbol/operator for power. Instead, Java provides a built-in helper tool in its `Math` class called `Math.pow()`.

---

## 🛠️ The Magic Tool: `Math.pow()`

The `Math` class in Java is like a toolbox filled with handy mathematical operations. To calculate power, we use the `pow()` method (short for power).

### 📌 Syntax
```java
Math.pow(base, exponent);
```

*   **`base`**: The number you want to multiply.
*   **`exponent`**: The number of times you want to multiply the base.
*   **Return Type**: It always gives you the answer back as a `double` (a decimal number).

### 📊 Visualizing `Math.pow(2, 3)`
| Base | Exponent | Math Formula | Calculation | Result |
| :--- | :--- | :--- | :--- | :--- |
| 2 | 3 | 2³ | 2 × 2 × 2 | 8.0 |

---

## 💻 Code Example: Using `Math.pow()`

Let's write a simple Java program to see this in action!

```java
public class PowerExample {
    public static void main(String[] args) {
        
        double base = 2.0;
        double exponent = 3.0;
        
        // Calculating 2 to the power of 3
        double result = Math.pow(base, exponent);
        
        System.out.println(base + " raised to the power of " + exponent + " is: " + result);
        
        // You can also use it directly with numbers!
        System.out.println("5 squared is: " + Math.pow(5, 2));
    }
}
```

**Output:**
```text
2.0 raised to the power of 3.0 is: 8.0
5 squared is: 25.0
```

---
##⚠️ Various Types of Math Methods
| Method | What it does | Example Input | Result |
| :--- | :--- | :--- | :--- |
| `Math.sqrt(x)` | Finds the square root | `Math.sqrt(100)` | `10.0` |
| `Math.max(x, y)` | Finds the larger number | `Math.max(10, 20)` | `20` |
| `Math.min(x, y)` | Finds the smaller number | `Math.min(10, 20)` | `10` |
| `Math.abs(x)` | Makes the number positive | `Math.abs(-45)` | `45` |
| `Math.round(x)` | Rounds to nearest integer | `Math.round(3.6)` | `4` |
---
## ⚠️ Important Concept: Type Casting (From Decimals to Integers)

**Notice something?** The result in the example above is `8.0`, not `8`. 

Because `Math.pow()` always returns a `double` (decimal) to handle negative exponents and fractions, what if you strictly want an integer (whole number)? 

You have to do something called **Type Casting**. It's like telling Java: *"I know this is a decimal, but please force it into a whole number box."*

```java
public class IntegerPower {
    public static void main(String[] args) {
        int base = 2;
        int exponent = 3;
        
        // We use (int) to cast/convert the decimal back to a whole number
        int result = (int) Math.pow(base, exponent);  //Explicit Type casting.
        
        System.out.println("The integer result is: " + result);
    }
}
```

**Output:**
```text
The integer result is: 8
```

---
