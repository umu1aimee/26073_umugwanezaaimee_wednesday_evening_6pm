# **Java Exception Handling Assignment**

This document describes the implementation of a Java-based project focused on simulating and handling common exceptions. The assignment is a practical exercise to deepen understanding of **exception handling** in Java through real-world scenarios.

---

## **Objective**

The primary aim of this assignment is to:
1. **Understand Exceptions in Java**:
   - Learn how exceptions occur in various scenarios during program execution.
2. **Simulate Exceptions**:
   - Create programs that deliberately trigger exceptions to observe their behavior.
3. **Handle Exceptions Gracefully**:
   - Use `try-catch` blocks to catch exceptions and prevent application crashes.
   - Apply `finally` blocks where cleanup operations are necessary.
4. **Develop Clear and Informative Code**:
   - Write meaningful comments and provide examples that are easy to understand.
   - Use scenarios that represent real-world problems.

By the end of this assignment, you will have a solid grasp of how exceptions can be used to build robust and error-resilient Java applications.

---

## **Exception Categories**

The exceptions are divided into two categories:

### **1. Checked Exceptions**
Checked exceptions are exceptions that are checked at compile time. These must be either handled using `try-catch` blocks or declared in the method signature using the `throws` keyword.

- **IOException**: Occurs during input/output operations, such as reading from or writing to a file.
- **FileNotFoundException**: A specific type of `IOException` thrown when an attempt to access a file fails because the file does not exist.
- **EOFException**: Occurs when the end of a file is reached unexpectedly during input operations.
- **SQLException**: Triggered by database-related errors such as invalid SQL queries or failed connections.
- **ClassNotFoundException**: Thrown when the Java Virtual Machine (JVM) cannot find a class file that is requested during runtime.

### **2. Unchecked Exceptions**
Unchecked exceptions, also known as runtime exceptions, occur during program execution and do not require explicit handling.

- **ArithmeticException**: Occurs when an illegal arithmetic operation is performed, such as division by zero.
- **NullPointerException**: Triggered when trying to access a field, method, or element on a `null` object reference.
- **ArrayIndexOutOfBoundsException**: Occurs when accessing an array element with an invalid index.
- **ClassCastException**: Thrown when an object is cast to an incompatible type.
- **IllegalArgumentException**: Occurs when a method receives an argument that is not valid or inappropriate.
- **NumberFormatException**: Triggered when attempting to convert a string into a numeric type, but the string format is invalid.

---

## **Program Structure**

### **Main Class**
The main class, `ExceptionHandler`, acts as the entry point of the program. It provides:
- An **interactive menu** that allows users to choose which exception to simulate.
- A **modular design**, where each exception simulation is implemented as a separate method.

### **Helper Methods**
Each exception has a dedicated method that:
1. **Triggers the Exception**: Simulates a scenario where the exception occurs naturally.
2. **Handles the Exception**: Uses `try-catch` blocks to catch the exception and provide appropriate solutions or feedback.
3. **Provides Explanations**: Includes comments and print statements to explain the scenario and handling mechanism.

---

## **Detailed Scenarios and Handling**

### **Checked Exceptions**
1. **IOException**  
   - **Scenario**: Simulates reading from a file that doesn’t exist.
   - **Code**: Uses a `FileReader` to open a non-existent file.
   - **Handling**: Catches `IOException` and provides an error message suggesting possible solutions (e.g., check the file path).
   
2. **FileNotFoundException**  
   - **Scenario**: Tries to access a missing file.
   - **Code**: Extends the `IOException` simulation by catching `FileNotFoundException` specifically.
   - **Handling**: Prompts the user to check the file path or create the file if missing.

3. **EOFException**  
   - **Scenario**: Reads beyond the end of a file.
   - **Code**: Simulates a file read operation where the end-of-file marker is reached unexpectedly.
   - **Handling**: Informs the user that no more content is available and prevents further read attempts.

4. **SQLException**  
   - **Scenario**: Tries to connect to a database with invalid credentials or execute invalid SQL commands.
   - **Code**: Uses `DriverManager` to attempt a connection to a non-existent database.
   - **Handling**: Catches `SQLException`, prints diagnostic information, and provides suggestions (e.g., check database credentials).

5. **ClassNotFoundException**  
   - **Scenario**: Simulates loading a class dynamically at runtime when the class is not available.
   - **Code**: Uses `Class.forName()` with an incorrect class name.
   - **Handling**: Catches `ClassNotFoundException` and suggests adding the missing class to the project.

---

### **Unchecked Exceptions**
6. **ArithmeticException**  
   - **Scenario**: Divides a number by zero.
   - **Code**: Demonstrates basic division operations that fail due to zero as a denominator.
   - **Handling**: Catches `ArithmeticException` and advises using a non-zero denominator.

7. **NullPointerException**  
   - **Scenario**: Accesses a method on a `null` object reference.
   - **Code**: Creates a `null` object and tries to call its method.
   - **Handling**: Catches `NullPointerException` and suggests initializing the object.

8. **ArrayIndexOutOfBoundsException**  
   - **Scenario**: Tries to access an array element with an invalid index.
   - **Code**: Creates an array and attempts to access indices outside its bounds.
   - **Handling**: Catches `ArrayIndexOutOfBoundsException` and displays valid index ranges.

9. **ClassCastException**  
   - **Scenario**: Casts an object to an incompatible type.
   - **Code**: Simulates invalid type casting operations.
   - **Handling**: Catches `ClassCastException` and enforces safe type checking.

10. **IllegalArgumentException**  
    - **Scenario**: Passes invalid arguments to a method (e.g., negative age for a person).
    - **Code**: Demonstrates parameter validation.
    - **Handling**: Catches `IllegalArgumentException` and provides user-friendly error messages.

11. **NumberFormatException**  
    - **Scenario**: Converts an invalid string to a number (e.g., "abc" to an integer).
    - **Code**: Uses `Integer.parseInt()` or `Double.parseDouble()` with invalid strings.
    - **Handling**: Catches `NumberFormatException` and asks for valid input.

---

## **How to Run**

1. Compile the program using:
   ```bash
   javac ExceptionHandler.java
   ```
2. Run the program:
   ```bash
   java ExceptionHandler
   ```
3. Choose an exception from the interactive menu and observe the output.

---

## **Grading Criteria**

The project is assessed based on:
1. **Correctness**: Are exceptions triggered and handled effectively?
2. **Clarity**: Is the code well-documented and easy to understand?
3. **Completeness**: Are all required exceptions simulated and explained?

---

## **Conclusion**

This assignment provides hands-on experience in handling both **checked** and **unchecked** exceptions in Java. It demonstrates the importance of exception handling in creating reliable and user-friendly applications.

**Author**: [Your Name]  
**Date**: December 2024
