# Assignment 1.4: Git Essentials I

## 1. Objective

The objective of this assignment is to convert a local project into a Git repository and learn how to track changes using Git commands and commits.

## 2. Introduction

Git is a version control system used to track changes in files and manage different versions of a project. It helps developers maintain a history of their work and collaborate with others.

A **repository** is a project folder tracked by Git. A **commit** is a saved snapshot of the project's tracked changes.

## 3. Procedure and Git Commands

### Step 1: Install Git

Download and install Git from the official website:

https://git-scm.com/downloads

Verify the installation by running:

```bash
git --version
```

If Git is installed correctly, the terminal displays its version number.

### Step 2: Open the Project Folder

Open the terminal in the `web-development-practice` project folder.

```bash
cd web-development-practice
```

If the terminal is already inside this folder, skip this command.

### Step 3: Initialize the Git Repository

```bash
git init
```

This command initializes a new Git repository in the project folder.

### Step 4: Configure Git Username and Email

Replace the example values with your own name and email address.

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

Verify the configuration:

```bash
git config --global user.name
git config --global user.email
```

### Step 5: Create an HTML File

Create a file named `index.html` in the project folder with the following code:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Git Project</title>
  </head>
  <body>
    <h1>Welcome to My Project</h1>
    <p>This project is managed using Git.</p>
  </body>
</html>
```

### Step 6: Check Repository Status

```bash
git status
```

This command displays the current state of the repository and identifies files that are untracked or modified.

### Step 7: Create Three Meaningful Commits

**Commit 1: Add the basic HTML page**

```bash
git add index.html
git commit -m "Create basic HTML page"
```

**Commit 2: Add a heading and paragraph**

Edit `index.html` and add or update the heading and paragraph:

```html
<h1>Welcome to My Project</h1>
<p>This project is managed using Git.</p>
<p>I am learning web development.</p>
```

Then run:

```bash
git add index.html
git commit -m "Add project introduction"
```

**Commit 3: Add page styling**

Create a file named `style.css` and write:

```css
body {
  font-family: Arial, sans-serif;
  margin: 40px;
  background-color: #f0f8ff;
}

h1 {
  color: navy;
}
```

Link the stylesheet inside the `<head>` section of `index.html`:

```html
<link rel="stylesheet" href="style.css" />
```

Save both files and run:

```bash
git add index.html style.css
git commit -m "Add basic page styling"
```

### Step 8: Verify the Commit History

Run the following commands:

```bash
git status
git log --oneline -3
```

The status should show a clean working tree if all changes have been committed. The log should display the three commits, with the newest commit first.

## 4. Important Git Commands

| Command | Purpose |
|---|---|
| `git init` | Initializes a Git repository |
| `git status` | Shows the current repository status |
| `git add` | Stages changes for a commit |
| `git commit` | Saves a snapshot of staged changes |
| `git log --oneline -3` | Displays the three latest commits |
| `git --version` | Checks the installed Git version |

## 5. Result

I successfully initialized a local Git repository, configured the Git username and email, created an HTML webpage, tracked file changes, and created three meaningful commits. I verified the repository status and commit history using Git commands.