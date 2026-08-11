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

---