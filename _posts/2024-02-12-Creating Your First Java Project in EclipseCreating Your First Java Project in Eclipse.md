---
layout: post
title: "Creating Your First Java Project in Eclipse"
date: 2024-02-12
categories: Java, Development, Eclipse
tags: Java, Eclipse, IDE, Tutorial
---

### Creating Your First Java Project in Eclipse

If you have Eclipse installed, follow these steps to create and run a simple "Hello, World!" Java project.

#### Step 1: Create a New Java Project

1. **Open Eclipse:**
   - Launch Eclipse and select your workspace directory.

2. **Create a New Java Project:**
   - Go to `File` > `New` > `Java Project`.
   - Enter a project name, e.g., `HelloWorldProject`.
   - Click `Finish`.

#### Step 2: Create a New Java Package

1. **Create a New Package:**
   - In the `Package Explorer` view, right-click on the `src` folder of your new project.
   - Select `New` > `Package`.
   - Enter the package name, e.g., `com.example`.
   - Click `Finish`.

#### Step 3: Create a New Java Class

1. **Create a New Class:**
   - Right-click on the `com.example` package you just created.
   - Select `New` > `Class`.
   - Enter the class name, e.g., `HelloWorld`.
   - Check the option `public static void main(String[] args)` to create a `main` method.
   - Click `Finish`.

2. **Write the Code:**
   - In the newly created `HelloWorld.java` file, you should see the following code:
     ```java
     package com.example;

     public class HelloWorld {
         public static void main(String[] args) {
             System.out.println("Hello, World!");
         }
     }
     ```

#### Step 4: Run Your Java Program

1. **Run the Program:**
   - Right-click on the `HelloWorld.java` file in the `Package Explorer`.
   - Select `Run As` > `Java Application`.

2. **View the Output:**
   - The output will appear in the `Console` view at the bottom of Eclipse, displaying:
     ```
     Hello, World!
     ```

#### Step 5: Troubleshooting

- **If the `Console` view is not visible**, go to `Window` > `Show View` > `Console` to open it.
- **Ensure your JDK is properly installed** and configured in Eclipse if you encounter any issues.

By following these steps, you will have successfully created and run a simple Java "Hello, World!" project in Eclipse. This process introduces you to the basic functionalities of Eclipse and Java development.

