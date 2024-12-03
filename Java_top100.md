# Core Java Interview Questions and Answers

| **Level** | **Question**                                                                 | **Answer**                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Easy**  | What are the main features of Java?                                         | Object-Oriented, Platform Independent, Secure, Robust, Multithreaded, High Performance.                                                                              |
| **Easy**  | Explain the difference between JDK, JRE, and JVM.                          | **JDK**: Tools for development. **JRE**: Libraries + JVM for running apps. **JVM**: Executes bytecode.                                                              |
| **Easy**  | What is a Class in Java?                                                   | A blueprint for objects containing fields and methods.                                                                                                              |
| **Easy**  | What are Wrapper Classes in Java?                                          | Provide object equivalents of primitive types (e.g., Integer for int, Character for char).                                                                           |
| **Easy**  | What is the difference between `==` and `equals()`?                        | `==`: Compares memory references. `equals()`: Compares object content.                                                                                              |
| **Easy**  | What is method overloading?                                                | Defining multiple methods with the same name but different parameter lists in the same class.                                                                        |
| **Easy**  | What is the purpose of the `static` keyword?                               | Makes a method or variable accessible without creating an object.                                                                                                   |
| **Easy**  | What is a constructor?                                                    | A special method that initializes an object.                                                                                                                        |
| **Easy**  | Can a constructor be private?                                              | Yes, used in Singleton or Factory patterns.                                                                                                                         |
| **Easy**  | What is garbage collection in Java?                                        | Automatic process by which JVM reclaims unused memory.                                                                                                              |
| **Easy**  | What is the `main()` method in Java?                                       | The entry point for Java programs: `public static void main(String[] args)`.                                                                                        |
| **Easy**  | What is the difference between an interface and a class?                  | Interfaces contain abstract methods; classes can have concrete implementations.                                                                                     |
| **Easy**  | What is typecasting in Java?                                              | Converting one data type to another (e.g., `int` to `double`).                                                                                                      |
| **Easy**  | What is the difference between `String` and `StringBuilder`?              | **String**: Immutable. **StringBuilder**: Mutable, better performance for concatenation.                                                                            |
| **Easy**  | What are Java Packages?                                                   | Packages are namespaces for organizing related classes and interfaces.                                                                                              |
| **Easy**  | Explain the `default` keyword in interfaces.                              | Allows defining default implementations for methods in interfaces.                                                                                                  |
| **Easy**  | What is `this` keyword in Java?                                           | Refers to the current instance of the class.                                                                                                                        |
| **Easy**  | What is the `super` keyword in Java?                                      | Refers to the immediate parent class object or methods.                                                                                                             |
| **Easy**  | Explain the difference between pass-by-value and pass-by-reference.       | Java is strictly pass-by-value. However, object references are passed, giving the illusion of pass-by-reference.                                                   |
| **Easy**  | What is the difference between `continue` and `break`?                   | **Break**: Terminates the loop. **Continue**: Skips the current iteration.                                                                                          |

---

| **Level** | **Question**                                                                 | **Answer**                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Medium**| What are Checked and Unchecked Exceptions?                                 | **Checked**: Compile-time (e.g., IOException). **Unchecked**: Runtime (e.g., NullPointerException).                                                                 |
| **Medium**| What is method overriding?                                                 | Redefining a method in a subclass with the same name and parameters as in the parent class.                                                                          |
| **Medium**| What is the difference between `ArrayList` and `LinkedList`?              | **ArrayList**: Backed by an array, better for indexing. **LinkedList**: Linked nodes, better for insertion/deletion.                                                |
| **Medium**| What are Generics in Java?                                                | Allows defining classes or methods with type parameters (e.g., `List<T>`).                                                                                         |
| **Medium**| Explain Serialization in Java.                                            | The process of converting an object into a byte stream for storage or transmission.                                                                                 |
| **Medium**| What is a functional interface in Java?                                   | An interface with a single abstract method (e.g., `Runnable`, `Comparable`).                                                                                       |
| **Medium**| What is the purpose of the `try-with-resources` statement?               | A statement that ensures automatic closing of resources (e.g., files, sockets).                                                                                     |
| **Medium**| What is `HashSet` in Java?                                                | A collection that contains unique elements and does not maintain any specific order.                                                                                |
| **Medium**| What is the difference between a Set and a List in Java?                 | **Set**: Unique elements, no order. **List**: Allows duplicates, maintains insertion order.                                                                         |
| **Medium**| What is multithreading in Java?                                           | Allows concurrent execution of two or more threads for multitasking.                                                                                               |
| **Medium**| What is the difference between `StringBuffer` and `StringBuilder`?        | **StringBuffer**: Thread-safe but slower. **StringBuilder**: Faster but not thread-safe.                                                                            |
| **Medium**| How does `synchronized` block work in Java?                               | Ensures that only one thread can access a block or method at a time by locking the object.                                                                          |
| **Medium**| What is the purpose of the `transient` keyword in Java?                  | Prevents serialization of fields marked as `transient`.                                                                                                             |
| **Medium**| How does a `TreeMap` work in Java?                                        | Stores key-value pairs in sorted order of the keys using Red-Black Tree implementation.                                                                             |
| **Medium**| What are the main methods of the `Object` class?                         | `toString()`, `equals()`, `hashCode()`, `wait()`, `notify()`, `clone()`.                                                                                           |

---

| **Level** | **Question**                                                                 | **Answer**                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hard**  | What is the purpose of the `volatile` keyword?                              | Ensures visibility of shared variables across threads by preventing caching.                                                                                        |
| **Hard**  | Explain Java's Memory Model (JMM).                                          | Defines how threads interact with memory, ensuring consistent and predictable behavior.                                                                             |
| **Hard**  | What is the difference between `wait()` and `sleep()`?                     | `wait()`: Releases lock, waits for notify. `sleep()`: Holds lock, pauses thread for set time.                                                                       |
| **Hard**  | What is the purpose of the `ForkJoinPool`?                                  | Used for parallelizing tasks by splitting them into subtasks and joining results.                                                                                   |
| **Hard**  | What is deadlock in Java?                                                  | A situation where two or more threads are waiting for each other's locks indefinitely.                                                                              |
| **Hard**  | How does Garbage Collection work in Java?                                  | Automatically reclaims memory occupied by unreachable objects using techniques like Mark-and-Sweep.                                                                 |
| **Hard**  | What is `CompletableFuture` in Java?                                       | A framework for asynchronous programming with callbacks, chaining, and exception handling.                                                                          |

---

| **Level**    | **Question**                                                                 | **Answer**                                                                                                                                                             |
|--------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Advanced** | What is a Singleton Pattern?                                               | A design pattern ensuring only one instance of a class exists. Implemented using private constructors and static methods.                                           |
| **Advanced** | Explain Reflection API.                                                    | Allows runtime inspection and manipulation of classes, methods, and fields.                                                                                        |
| **Advanced** | What is a WeakReference in Java?                                           | A reference type that does not prevent an object from being garbage collected.                                                                                     |
| **Advanced** | What is the difference between `parallelStream` and `stream`?            | `parallelStream` executes operations in multiple threads, whereas `stream` uses a single thread.                                                                   |
| **Advanced** | Explain the Observer design pattern in Java.                              | Defines a one-to-many dependency so that when one object changes state, all its dependents are notified.                                                           |
| **Advanced** | What is the Decorator Pattern?                                             | A structural design pattern used to dynamically add behavior to an object.                                                                                         |
