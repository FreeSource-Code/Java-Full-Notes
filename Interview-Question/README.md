# 📚 Java Interview Questions & Answers

This file contains important Java interview questions with answers for freshers and intermediate learners. Great for internship and job preparation.

---

## 🧠 Core Java

### 1. What are the features of Java?
- Object-Oriented
- Platform Independent
- Secure & Robust
- High Performance
- Multithreaded
- Distributed

### 2. What is the difference between JDK, JRE, and JVM?
- **JDK:** Java Development Kit (includes JRE + tools)
- **JRE:** Java Runtime Environment (includes JVM + libraries)
- **JVM:** Java Virtual Machine (executes bytecode)

### 3. Difference between `==` and `.equals()`?
- `==`: Compares references (memory location)
- `.equals()`: Compares values/content

### 4. What is a constructor? Types?
- Special method called when an object is created.
- **Types**: Default, Parameterized, Copy constructor

### 5. What is the difference between method overloading and overriding?
- **Overloading:** Same method name, different parameters (compile-time)
- **Overriding:** Same method, same parameters in child class (runtime)

### 6. What is the final keyword?
- Final **variable**: Constant
- Final **method**: Cannot be overridden
- Final **class**: Cannot be inherited

---

## 🧩 OOPs Concepts

### 7. Four pillars of OOP?
- Encapsulation
- Abstraction
- Inheritance
- Polymorphism

### 8. Difference between Abstraction and Encapsulation?
- **Abstraction:** Hides implementation using interfaces/abstract classes
- **Encapsulation:** Hides data using private variables and public methods

### 9. Can Java support multiple inheritance?
- Java supports it via **interfaces**, not with classes.

---

## 🔁 Collections

### 10. Difference between List, Set, and Map?
- **List:** Ordered, allows duplicates
- **Set:** Unordered, no duplicates
- **Map:** Key-value pairs, keys are unique

### 11. Difference between HashMap and LinkedHashMap?
- **HashMap:** No order
- **LinkedHashMap:** Maintains insertion order

### 12. What is the difference between Array and ArrayList?
- **Array:** Fixed size, can hold primitives
- **ArrayList:** Dynamic, only objects

---

## ⚠️ Exception Handling

### 13. What is the difference between checked and unchecked exceptions?
- **Checked:** Compile-time (e.g., IOException)
- **Unchecked:** Runtime (e.g., NullPointerException)

### 14. What is the purpose of `finally` block?
- Always executes after try/catch, used for cleanup

### 15. Difference between throw and throws?
- `throw`: Used to throw an exception
- `throws`: Declares exceptions a method may throw

---

## 🧵 Multithreading

### 16. Ways to create a thread?
- Extend `Thread` class
- Implement `Runnable` interface

### 17. What is synchronization?
- Prevents thread interference by allowing one thread to access a block at a time.

### 18. Difference between `wait()` and `sleep()`?
- `wait()` releases lock, used for communication
- `sleep()` holds lock, just pauses thread

---

## 🚀 Java 8 Features

### 19. What is a Functional Interface?
- Interface with only one abstract method, e.g., Runnable, Callable

### 20. What is Stream API?
- Processes collections in a functional style

```java
List<String> names = list.stream().filter(s -> s.startsWith("A")).collect(Collectors.toList());
```
### 24. What is Garbage Collection in Java?
- Garbage Collection (GC) is the process by which Java automatically manages memory by destroying unused objects.

It helps in avoiding memory leaks.

GC is done by the JVM.

###25. What is the transient keyword?
-The transient keyword is used to indicate that a variable should not be serialized.

```java
Copy
Edit
class Student implements Serializable {
    int id;
    transient String password; // won't be saved in file
}
```
### 26. What is the volatile keyword?
-The volatile keyword ensures visibility of changes to variables across threads.

```java
Copy
Edit
public class Example {
    private volatile boolean flag = true;
}
```
### 27. What are wrapper classes?
-Wrapper classes convert primitive types into objects.

-Primitive	Wrapper Class
-int	Integer
-double	Double
-char	Character

### 28. What is autoboxing and unboxing?
-Autoboxing: Converting primitive to object automatically.

-Unboxing: Converting object back to primitive.
```
int a = 10;
Integer obj = a; // autoboxing

int b = obj;     // unboxing
````

### 29. What is the difference between compile-time and runtime polymorphism?
-Compile-time Polymorphism: Method overloading.

Runtime Polymorphism: Method overriding.

```java
Copy
Edit
// Compile-time
void add(int a, int b) {}
void add(double a, double b) {}

// Runtime
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}
class Dog extends Animal {
    void sound() {
        System.out.println("Bark");
    }
}
```
