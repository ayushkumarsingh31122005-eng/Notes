# ☕ Java Inner Classes: A Beginner's Guide

Welcome! Today we are going to learn about one of Java's very useful features: **Inner Classes**. 





## 1. What is an Inner Class?

In Java, we normally write one class per file. But Java allows us to write **a class inside another class**. This inside class is called an "Inner Class" (or Nested Class).

### 🏠 A Simple Visual Analogy
Think of a **House**. 
A House has walls, a roof, and a front door. 
Inside the House, there is a **Bedroom**. 
The Bedroom is completely inside the House. It belongs to the House. You usually don't put a Bedroom out on the street!

```text
+---------------------------------------+
|  OUTER CLASS (The House)              |
|                                       |
|  - Address                            |
|  - Door Color                         |
|                                       |
|      +-------------------------+      |
|      |  INNER CLASS (Bedroom)  |      |
|      |                         |      |
|      |  - Bed                  |      |
|      |  - Lamp                 |      |
|      +-------------------------+      |
|                                       |
+---------------------------------------+
```

### Why do we use them?
1. **Grouping logically:** If a class is only useful to one other class, keep them together! (Like the Bedroom inside the House).
2. **Secret Access:** An Inner Class can see all the private secrets (variables and methods) of the Outer Class.

---

## 2. The Four Types of Inner Classes

There are exactly 4 ways to write a class inside another class in Java. Let's look at them one by one.

### Type 1: Member Inner Class (The standard one)
This is a normal class written inside another class. It is not `static`. 

**Rule:** To create this inner class, you MUST create the outer class first.

```java
// 1. The Outer Class
class Car {
    private String carName = "Mustang"; // A private secret!

    // 2. The Inner Class
    class Engine {
        void startEngine() {
            // The inner class can see the private variable 'carName'
            System.out.println("Starting the engine of the " + carName);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        // Step A: Create the Outer Object
        Car myCar = new Car();
        
        // Step B: Create the Inner Object using the Outer Object
        Car.Engine myEngine = myCar.new Engine();
        
        myEngine.startEngine(); // Output: Starting the engine of the Mustang
    }
}
```

### Type 2: Static Nested Class
This class has the word `static` written in front of it. 
Because it is static, **it does NOT need the Outer Class object to be created first.** 

*Note: Because it doesn't need the outer object, it CANNOT see the non-static private variables of the outer class.*

```java
class Computer {
    // Static Inner Class
    static class USB {
        void connect() {
            System.out.println("USB is connected!");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        // We do NOT need to create a Computer object first!
        // We can just create the USB directly using the class name.
        Computer.USB myUsb = new Computer.USB();
        myUsb.connect(); // Output: USB is connected!
    }
}
```

### Type 3: Local Inner Class (Inside a Method)
Sometimes, you only need a class for a few lines of code inside a specific method. You can write a class *inside* a method!

```java
class Bank {
    void processPayment() {
        
        // A class hidden inside a method!
        class PaymentValidator {
            void check() {
                System.out.println("Payment is valid.");
            }
        }

        // We must use it right here inside the method
        PaymentValidator validator = new PaymentValidator();
        validator.check();
    }
}
```

### Type 4: Anonymous Inner Class (The one with no name!)
This is the most famous one. "Anonymous" means "no name". We use this when we want to override a method of a class or interface very quickly, just for one time, without making a whole new separate file.

```java
// A simple Animal class
class Animal {
    void makeNoise() {
        System.out.println("Some sound");
    }
}

public class Main {
    public static void main(String[] args) {
        
        // We create an Animal, but we instantly change how it works using { }
        // This creates a nameless (anonymous) class on the spot!
        Animal dog = new Animal() {
            @Override
            void makeNoise() {
                System.out.println("Woof! Woof!");
            }
        }; // Notice the semicolon here!

        dog.makeNoise(); // Output: Woof! Woof!
    }
}
```

---

## 📝 Quick Summary for Beginners

*   **Member Inner:** Normal inside class. Needs the outer object first.
*   **Static Nested:** Static inside class. Doesn't need the outer object first.
*   **Local Inner:** Class inside a method. Only exists inside that method.
*   **Anonymous Inner:** Class without a name. Used for quick, one-time overrides.

Take your time reading the code examples, write them out in your own Java editor, and run them. That is the best way to learn! Let me know when you are ready to learn more!