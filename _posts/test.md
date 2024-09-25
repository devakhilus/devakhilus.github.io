---
layout: post
title: "Using EGit in Eclipse for GitHub Integration"
date: 2024-09-16
categories: Git, Eclipse, Development
tags: Git, Eclipse, EGit, Tutorial
---





# Using EGit in Eclipse for GitHub Integration

## 1. Install EGit Plugin (if not already installed)

EGit is the Git integration for Eclipse. Most Eclipse IDEs come with it pre-installed, but if not, you can install it from the Eclipse Marketplace.

- Go to **Help** > **Eclipse Marketplace**.
- Search for **"EGit"** and install it.

## 2. Create a Git Repository

### Open Your Project in Eclipse

- Open Eclipse and navigate to your project in the **Project Explorer**.

### Initialize Git Repository

- Right-click on your project and select **Team** > **Share Project...**.
- Select **Git** and click **Next**.
- Click **Create** to initialize a new Git repository in your project’s directory.
- Click **Finish**.

## 3. Commit Your Changes

### Stage Your Changes

- Right-click on your project again, go to **Team** > **Commit...**.
- In the **"Commit Changes"** window, you can review the changes and select the files you want to commit.
- Write a commit message in the **"Commit Message"** field.
- Click **Commit**.

## 4. Push to GitHub

### Add Remote Repository

- Right-click on your project, select **Team** > **Remote** > **Push...**.
- In the **"Push to Remote Repository"** window, click **Add All Branches Specified Below**.
- Enter the URL of your GitHub repository. If you don’t have one, you can create it on GitHub.
- Click **Next**.

### Authentication

- You may be prompted to enter your GitHub credentials (username and password or a personal access token).
- Click **Finish**.

### Push Changes

- After adding the remote repository, you can push your commits.
- Right-click on your project, go to **Team** > **Push to Upstream**.
- Confirm by clicking **OK** or **Finish**.
