---
layout: post
title: "Static vs Dynamic Type Checking"
date: 2024-02-08
categories: Java, Full-Stack, Roadmap, java intro
tags: Java, Full-Stack, Development, Learning Path, Skills
---

### Type Checking

**Type checking** is a process that ensures the data types of variables, expressions, and function returns are used correctly in a program. This process can occur at two main stages:

1. **Static Type Checking**: Occurs at compile time.
2. **Dynamic Type Checking**: Occurs at run time.

### Static Type Checking

- **What It Is:**  
  Static type checking is the process of verifying the types of variables, functions, and expressions during the compilation of the program. Languages like Java, C++, and Swift use static type checking.
  
- **Process:**  
  - The compiler checks the types of variables, expressions, and function arguments before the program is executed.
  - If a type mismatch or error is found, the program will not compile, preventing runtime type-related errors.
  
- **Advantages:**  
  - **Early Error Detection:** Errors are caught early in the development process, making debugging easier.
  - **Performance:** Since type checking is done during compilation, the resulting code is typically faster at runtime.
  - **Type Safety:** Helps in ensuring that type constraints are not violated, enhancing code reliability and reducing bugs.

- **Example (Java):**
  ```java
  int number = "Hello";  // Compilation error: incompatible types


### Dynamic Type Checking

- **What It Is:**  
  Dynamic type checking occurs during runtime, meaning the types of variables and expressions are checked as the program is being executed. Languages like Python, JavaScript, and Ruby use dynamic type checking.

- **Process:**  
  - The interpreter checks the types of variables and expressions at runtime when they are used.
  - Type errors are detected only when the code is executed, which may lead to runtime errors if type mismatches occur.

- **Advantages:**  
  - **Flexibility:** Allows variables to change types, making the code more adaptable and easier to write.
  - **Ease of Use:** No need to specify types explicitly, making the syntax simpler and the code easier to modify.

- **Disadvantages:**  
  - **Runtime Errors:** Errors are discovered only when the affected code is executed, which can lead to failures in production if not properly tested.
  - **Performance Overhead:** Dynamic checks add extra overhead during execution, which can make programs slower compared to statically typed languages.

- **Example (Python):**
  ```python
  number = "Hello"  # Allowed at assignment time
  print(number + 5)  # Runtime error: TypeError: can only concatenate str (not "int") to str


### Key Differences

- **Timing:**  
  - **Static Type Checking:** Occurs at compile time.
  - **Dynamic Type Checking:** Occurs at runtime.

- **Error Handling:**  
  - **Static Type Checking:** Catches type errors before execution.
  - **Dynamic Type Checking:** Catches errors during execution.

- **Performance:**  
  - **Static Type Checking:** Usually results in faster code execution.
  - **Dynamic Type Checking:** Can slow down execution due to type checks at runtime.

Understanding these differences helps developers choose the right language and approach based on their project's needs and performance requirements!