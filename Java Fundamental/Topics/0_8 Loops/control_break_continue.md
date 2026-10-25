# Java Loop Control: `break` and `continue`

Welcome to the world of loop control! Whenever we use loops (`for`, `while`, or `do-while`) in Java, they normally run until their condition becomes `false`. 

But what if you want to **stop early**? Or what if you want to **skip one specific turn** but keep going? That is exactly where `break` and `continue` come in.

---

## 1. The `break` Keyword

The `break` keyword acts like an **emergency exit** for your loop. When Java sees the word `break`, it immediately destroys the loop and moves on to the code that comes *after* the loop.

### Real-Life Analogy
Imagine you are searching through a box of 10 apples to find the *one* green apple. Once you find the green apple on your 3rd try, do you keep looking at the rest of the apples? No! You **break** out of your search because you found what you needed.

### Visual Flowchart

```text
       Start Loop
           |
           V
    [Condition true?] ---> NO ---> (Exit Loop)
           |
          YES
           |
           V
  ---> Is it time to break? ---> YES ---> [BREAK!] ---> (Exit Loop Immediately)
  |        |
  |       NO
  |        |
  |        V
  ---- [Run Loop Code]
```

### Code Example
Let's write a loop that counts from 1 to 10, but we want it to stop completely when it reaches 5.

```java
public class BreakExample {
    public static void main(String[] args) {
        
        for (int i = 1; i <= 10; i++) {
            
            if (i == 5) {
                System.out.println("Emergency Exit! We hit 5.");
                break; // This kicks us out of the loop!
            }
            
            System.out.println("Current number: " + i);
        }
        
        System.out.println("Loop has finished.");
    }
}
```

**Output:**
```text
Current number: 1
Current number: 2
Current number: 3
Current number: 4
Emergency Exit! We hit 5.
Loop has finished.
```
*Notice how 5, 6, 7, 8, 9, and 10 are NEVER printed. The loop died at 5.*

---

## 2. The `continue` Keyword

The `continue` keyword acts like a **skip button**. When Java sees `continue`, it skips the rest of the code for *that specific turn*, and jumps straight back to the top to start the next turn.

### Real-Life Analogy
Imagine you are eating a bowl of grapes. You pick them up one by one. If you pick up a sour grape, you throw it away (skip it) and **continue** eating the rest of the good grapes. You don't stop eating entirely; you just skipped that one bad grape.

### Visual Flowchart

```text
       Start Loop
           |
           V
    [Condition true?] ---> NO ---> (Exit Loop)
           |
          YES
           |
           V
  ---> Is it time to continue? ---> YES ---> [CONTINUE!] --
  |        |                                              |
  |       NO                                              |
  |        |                                              |
  |        V                                              |
  |    [Run Loop Code]                                    |
  |        |                                              |
  ---------<-----------------------------------------------
  (Go back to the top for the next turn)
```

### Code Example
Let's write a loop that counts from 1 to 5, but we want to skip the number 3.

```java
public class ContinueExample {
    public static void main(String[] args) {
        
        for (int i = 1; i <= 5; i++) {
            
            if (i == 3) {
                System.out.println("Skipping number 3!");
                continue; // This skips the code below and jumps to the next 'i'
            }
            
            System.out.println("Current number: " + i);
        }
        
        System.out.println("Loop has finished.");
    }
}
```

**Output:**
```text
Current number: 1
Current number: 2
Skipping number 3!
Current number: 4
Current number: 5
Loop has finished.
```
*Notice how it skipped printing "Current number: 3", but it still finished counting 4 and 5.*

---

## 3. Quick Summary Comparison

| Keyword | What it does | When to use it |
| :--- | :--- | :--- |
| **`break`** | Stops the entire loop forever. | When you have found what you are looking for, or an error happens and you must stop looping. |
| **`continue`**| Stops the *current turn* and goes to the next turn. | When you want to filter out specific items or skip bad data, but keep processing the rest. |

---

## 4. Related Topic: "Labeled" Break and Continue (For Nested Loops)

As a beginner, you mostly use simple loops. But soon you will learn about **Nested Loops** (a loop inside a loop). 

Normally, a `break` only stops the *closest* loop. If you want to break out of a massive outer loop from the inside, you can give your loops "names" (called labels).

**Example of Syntax:**
```java
outerLoop: // This is a label
for(int i = 1; i <= 3; i++) {
    for(int j = 1; j <= 3; j++) {
        if(i == 2 && j == 2) {
            break outerLoop; // This breaks the big outer loop, not just the inner one!
        }
    }
}
```
*Don't worry too much about labels right now, just know that they exist for when your code gets more advanced!*