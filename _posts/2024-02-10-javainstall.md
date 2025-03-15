---
layout: post
title: "Installing Java for Development on Windows and Linux"
date: 2024-02-10
categories: Java, Full-Stack, Roadmap, java intro
tags: Java, Full-Stack, Development, Learning Path, Skills
---

### Installing Java for Development

To begin Java development, you need to install the Java Development Kit (JDK). Below are the steps for installing the JDK on Windows and Linux systems.

#### Installing Java on Windows

1. **Download the JDK:**
   - Visit the [Oracle JDK Downloads page](https://www.oracle.com/java/technologies/javase-downloads.html) or the [AdoptOpenJDK Downloads page](https://adoptium.net/).
   - Choose the latest JDK version compatible with Windows and download the installer.

2. **Run the Installer:**
   - Double-click the downloaded `.exe` file to start the installation.
   - Follow the installation wizard, accepting the default settings or modifying them as needed.
   - The JDK will be installed in a default directory like `C:\Program Files\Java\jdk-<version>`.

3. **Set Up Environment Variables:**
   - Open the Start Menu, search for `Environment Variables`, and select `Edit the system environment variables`.
   - Click on the `Environment Variables` button.
   - Under `System Variables`, click `New` and add a variable named `JAVA_HOME` with the path to your JDK installation directory (e.g., `C:\Program Files\Java\jdk-<version>`).
   - Find the `Path` variable in the `System variables` section, select it, and click `Edit`. Add a new entry with `%JAVA_HOME%\bin`.

4. **Verify the Installation:**
   - Open Command Prompt and type `java -version` and `javac -version` to confirm that Java is installed correctly.

#### Installing Java on Linux

1. **Update Package Index:**
   - Open a terminal window and run the following command to update your package index:
     ```bash
     sudo apt update
     ```

2. **Install the JDK:**
   - For Ubuntu/Debian-based distributions:
     ```bash
     sudo apt install openjdk-17-jdk
     ```
   - For Fedora/RHEL-based distributions:
     ```bash
     sudo dnf install java-17-openjdk-devel
     ```

   - Alternatively, you can download and install the Oracle JDK from the [Oracle JDK Downloads page](https://www.oracle.com/java/technologies/javase-downloads.html) and follow the installation instructions.

3. **Set Up Environment Variables:**
   - Edit the `~/.bashrc` or `~/.profile` file to include the `JAVA_HOME` variable:
     ```bash
     export JAVA_HOME=/usr/lib/jvm/java-17-openjdk
     export PATH=$JAVA_HOME/bin:$PATH
     ```
   - Apply the changes by running:
     ```bash
     source ~/.bashrc
     ```

4. **Verify the Installation:**
   - Open a terminal and type `java -version` and `javac -version` to confirm that Java is installed correctly.

#### Changing the Java Version on Linux

##### For Debian-based Distributions (e.g., Ubuntu):

1. **List Installed JDK Versions:**
   ```bash
   sudo update-java-alternatives --list
   ```
