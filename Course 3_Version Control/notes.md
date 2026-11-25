# Notes — Version Control

This file contains my learning notes from the **Version Control** course in the Meta Full-Stack Development learning path.

Version control is one of the most important tools in software development because it helps developers track changes, collaborate safely, manage project history, and recover earlier versions of a project.

---

## 📚 Course Modules

| No. | Module                 | Focus                                                                          |
| --- | ---------------------- | ------------------------------------------------------------------------------ |
| 01  | Software Collaboration | Understanding teamwork, version control systems, and collaboration workflows   |
| 02  | Command Line           | Learning basic terminal commands used in software development                  |
| 03  | Work with Git          | Practicing Git commands, repositories, commits, branches, and GitHub workflows |

---

# Module 1: Software Collaboration

## What is Software Collaboration?

Software collaboration means working with other developers on the same software project.

In real software development, teams often work together on different parts of the same project, such as:

- Front-end development
- Back-end development
- Database design
- Bug fixing
- Testing
- Documentation
- New feature development

Version control makes collaboration safer because it tracks changes and helps prevent developers from accidentally overwriting each other’s work.

---

## What is Version Control?

Version control is a system that tracks changes in files over time.

It allows developers to:

- Save different versions of a project
- Track changes
- See who changed what
- Return to previous versions
- Work safely with other developers
- Manage changes in code

Without version control, projects can become confusing with file names like:

project-final
project-final-new
project-final-real-final
project-final-final-2

---

## Why Version Control is Important

Version control is important because software projects change constantly.

It helps developers:

- Keep a complete history of changes
- Understand what changed and when
- Fix mistakes safely
- Work on new features without breaking the main project
- Collaborate with other developers
- Review changes before adding them to the main codebase
- Restore old versions if something goes wrong

In professional software development, version control is not optional. It is a basic tool used by developers, testers, project teams, and companies.

---

## Centralized vs Distributed Version Control

There are two main types of version control systems:

| Type                               | Meaning                                                      | Examples        |
| ---------------------------------- | ------------------------------------------------------------ | --------------- |
| Centralized Version Control System | Uses one central server that stores the main project history | CVS, Subversion |
| Distributed Version Control System | Every user has a full local copy of the project history      | Git, Mercurial  |

---

## Centralized Version Control System

A Centralized Version Control System, or CVCS, uses a central server to store the main repository.

Developers connect to the central server to access and update the project.

### Key Features

- One central repository
- Users depend on the server
- Most operations require server connection
- Performance can be slower because the server must be contacted often

### Examples

- Concurrent Versions System, CVS
- Subversion, SVN

### Main Limitation

If the central server is unavailable, developers may not be able to access the latest version of the project or perform many important operations.

---

## Distributed Version Control System

A Distributed Version Control System, or DVCS, gives every user a full local copy of the repository.

This means developers can work locally without needing to connect to the server all the time.

### Key Features

- Every user has a full copy of the repository
- Local operations are faster
- Developers can commit changes offline
- The server is mainly needed for sharing work through push and pull

### Examples

- Git
- Mercurial

### Why DVCS is Faster

DVCS is usually faster because many actions happen locally on the developer’s computer instead of needing constant communication with a central server.

---

## Git vs GitHub

### Git was created by Linus Torvalds in 2005 to manage the Linux kernel source code efficiently as a fast, distributed version control system.

| Tool   | Meaning                                                                      |
| ------ | ---------------------------------------------------------------------------- |
| Git    | A version control system used to track changes locally                       |
| GitHub | An online platform used to store, share, and collaborate on Git repositories |

### Simple Difference

Git tracks changes on my computer.
GitHub stores and shares my project online. (Git Hub is cloud based)

Git was developed by Linus Torvalds in 2005 to manage the source code of the Linux kernel.

Git is the tool that manages source code history.
GitHub is the platform that hosts repositories online.

---

## Version Control as a Time Machine

Version control systems like Git work like a project time machine.

Git saves project history through commits. Each commit is like a checkpoint.

Example:

- Commit 1: Create homepage
- Commit 2: Add navigation bar
- Commit 3: Add contact form
- Commit 4: Fix styling issue

If something breaks, developers can check earlier versions, compare changes, or restore a previous working version.

---

## Why Git is Universal

Git is useful for many types of developers because it tracks file changes, not only one programming language.

Git can be used for:

- Web development
- Mobile development
- Game development
- Database projects
- API projects
- AI projects
- Documentation
- Team collaboration

### Easy Memory Trick

- Git = project time machine
- Commit = saved checkpoint
- Branch = safe workspace
- Merge = combine changes
- GitHub = online project storage

---

## How Version Control Helps Resolve Conflicts

Version control helps manage situations where multiple developers change the same code.

A conflict happens when Git cannot automatically decide which change should be kept.

### Example Conflict Situation

Original code:

```js
const message = "Welcome to our website";
```

---

# Module 2: Command Line

## What is the Command Line?

The command line is a text-based way to interact with the computer.

Instead of clicking folders, buttons, and menus, developers type commands to perform tasks.

The command line is commonly used for:

- Navigating folders
- Creating files and folders
- Running programs
- Installing tools
- Using Git
- Managing software projects

---

## Why Developers Use the Command Line

Developers use the command line because many programming tools are designed to work through commands.

The command line helps developers work faster and gives more control over projects.

Git is often used through the command line, so learning basic command line commands is important for version control.

---

## Command Line vs Graphical User Interface

| Interface                | Meaning                                 |
| ------------------------ | --------------------------------------- |
| Command Line Interface   | Uses typed commands                     |
| Graphical User Interface | Uses windows, buttons, icons, and menus |

A graphical interface is easier for beginners, but the command line is powerful and widely used in software development.

---

## Basic Command Line Commands

| Command             | Purpose                                  |
| ------------------- | ---------------------------------------- |
| `pwd`               | Shows the current folder location        |
| `ls`                | Lists files and folders on macOS/Linux   |
| `dir`               | Lists files and folders on Windows       |
| `cd folder-name`    | Moves into a folder                      |
| `cd ..`             | Moves back one folder                    |
| `mkdir folder-name` | Creates a new folder                     |
| `touch file-name`   | Creates a new file on macOS/Linux        |
| `echo. > file-name` | Creates a new file on Windows PowerShell |
| `clear`             | Clears the terminal on macOS/Linux       |
| `cls`               | Clears the terminal on Windows           |

## Windows Command Prompt vs Bash

In Windows Command Prompt, some Bash commands do not work.

| Task                   | Bash Command        | Windows Command Prompt |
| ---------------------- | ------------------- | ---------------------- |
| Show current location  | `pwd`               | `cd`                   |
| List files and folders | `ls`                | `dir`                  |
| Move into folder       | `cd folder-name`    | `cd folder-name`       |
| Move back one folder   | `cd ..`             | `cd ..`                |
| Create folder          | `mkdir folder-name` | `mkdir folder-name`    |

If I want to use Bash-style commands like `pwd` and `ls` on Windows, I can use Git Bash instead of Command Prompt.

---

## Example Command Line Workflow

```bash
cd Documents
mkdir version-control-practice
cd version-control-practice
```

## Command Line: Standard Input, Output, and Error

In the command line, programs communicate using standard streams.

These streams are not specific to Python. They are general command line concepts used by many programs, tools, and programming languages.

Examples include:

- Bash commands
- Git commands
- C programs
- C++ programs
- Python programs
- Node.js programs
- System tools

---

## Three Standard Streams

| Number | Stream Name     | Short Name | Meaning                       |
| ------ | --------------- | ---------- | ----------------------------- |
| `0`    | Standard Input  | `stdin`    | Input given to a program      |
| `1`    | Standard Output | `stdout`   | Normal output from a program  |
| `2`    | Standard Error  | `stderr`   | Error messages from a program |

---

## 0 — Standard Input

Standard Input, or `stdin`, is the information given to a program.

It usually comes from the keyboard, but it can also come from another command or a file.

Simple meaning:

`0 = input`

Example idea:

A program asks for a name.  
The user types the name.  
That typed value is standard input.

---

## 1 — Standard Output

Standard Output, or `stdout`, is the normal result produced by a program.

It usually appears on the terminal screen.

Simple meaning:

`1 = normal output`

Example:

`echo Hello`

Output:

`Hello`

The word `Hello` is standard output.

---

## 2 — Standard Error

Standard Error, or `stderr`, is used for error messages.

It is separate from normal output so that errors can be handled differently.

Simple meaning:

`2 = error output`

Example:

If I type a wrong command, the terminal may show an error message.

That error message is standard error.

---

## Why Standard Error is Separate

Standard error is separate from standard output because normal results and error messages are different.

This helps developers:

- Understand command results clearly
- Save normal output to one file
- Save errors to another file
- Debug problems more easily
- Separate successful output from failed output

---

## Easy Memory Trick

| Number | Meaning                |
| ------ | ---------------------- |
| `0`    | Input comes in         |
| `1`    | Normal output goes out |
| `2`    | Error output goes out  |

Simple memory:

`0 = input`  
`1 = output`  
`2 = error`

---

## Redirection Basics

Output can be redirected to files.

### Redirect standard output

`command > output.txt`

This sends normal output, stream `1`, into a file.

Example:

`echo Hello > message.txt`

This writes `Hello` into `message.txt`.

---

### Redirect standard error

`command 2> error.txt`

This sends error output, stream `2`, into a file.

Example:

`wrongcommand 2> error.txt`

This saves the error message into `error.txt`.

---

## Summary

Standard input, standard output, and standard error are general command line concepts.

They help programs receive input, show normal results, and report errors.

## These streams are used across many programming languages and command line tools, not only Python.

## Grep Command

`grep` is a command-line tool used to search for specific text patterns inside files or command output.

It is commonly used by developers to quickly find words, errors, functions, or specific lines in files.

### Basic Syntax

`grep "text" file-name`

### Example

`grep "error" log.txt`

This searches for the word `error` inside the file `log.txt`.

---

## Why `grep` is Useful

`grep` helps developers:

- Search inside files quickly
- Find errors in log files
- Find specific words or code
- Filter command output
- Debug problems faster

---

## Example

If a file contains:

````text
Login successful
Error: password incorrect
User logged out

Command: grep "Error" log.txt
Output: Error: password incorrect
````
## Summary

grep = find text inside files

On Windows Command Prompt, `grep` usually does **not** work by default. 
In Windows, similar command is:

```cmd
findstr "error" log.txt
````

---

# Module 3: Work with Git

## Module Focus

This module focuses on using Git in practice.

After learning what version control is in Module 1, this module explains how to actually work with Git commands, repositories, commits, branches, and remote repositories.

---

## Basic Git Workflow

The basic Git workflow is:

1. Create or edit files
2. Check the project status
3. Add files to the staging area
4. Commit the changes
5. Push the changes to GitHub

Example:

```bash
git status
git add .
git commit -m "Add version control notes"
git push
````

## Working Directory, Staging Area, and Repository

Git has three important areas:

| Area              | Meaning                                              |
| ----------------- | ---------------------------------------------------- |
| Working Directory | The folder where I edit my project files             |
| Staging Area      | The place where I prepare files before committing    |
| Repository        | The place where Git stores committed project history |

### Simple Flow

Edit files
→ Stage files
→ Commit files

---

## Important Git Commands

| Command                       | Purpose                                         |
| ----------------------------- | ----------------------------------------------- |
| `git init`                    | Starts a new Git repository                     |
| `git status`                  | Shows the current state of the project          |
| `git add .`                   | Adds all changed files to the staging area      |
| `git add file-name`           | Adds one specific file to the staging area      |
| `git commit -m "message"`     | Saves a checkpoint with a message               |
| `git log`                     | Shows commit history                            |
| `git branch`                  | Shows existing branches                         |
| `git checkout -b branch-name` | Creates and switches to a new branch            |
| `git merge branch-name`       | Combines another branch into the current branch |
| `git clone repo-url`          | Copies a remote repository to my computer       |
| `git pull`                    | Downloads the latest changes from GitHub        |
| `git push`                    | Uploads local commits to GitHub                 |

---

## Git Repository

A repository is a project folder that Git tracks.

To create a new Git repository, use:

`git init`

This command starts tracking the current folder with Git.

---

## Git Status

`git status` shows what has changed in the project.

It helps me see:

- Modified files
- New untracked files
- Files staged for commit

Command:

`git status`

---

## Git Add

`git add` moves files to the staging area.

To stage all changed files:

`git add .`

To stage one specific file:

`git add notes.md`

---

## Git Commit

A commit is a saved checkpoint of the project.

Example:

`git commit -m "Add notes for version control"`

A good commit message should clearly explain what changed.

### Good Commit Message Examples

- Add homepage structure
- Fix navigation bar styling
- Update version control notes
- Create README file

---

## Git Log

`git log` shows the commit history.

Command:

`git log`

This helps me review previous commits and understand the project timeline.

---

## Git Branch

A branch is a separate workspace for changes.

Branches are useful when working on new features without changing the main project immediately.

Example:

`git checkout -b login-page`

This creates and switches to a new branch called `login-page`.

---

## Git Merge

Merge means combining changes from one branch into another.

Example:

`git merge login-page`

This brings the changes from the `login-page` branch into the current branch.

---

## Git Clone

Clone means copying a repository from GitHub to my computer.

Example:

`git clone repository-url`

This creates a local copy of an online repository.

---

## Git Pull

Pull means downloading the latest changes from the remote repository.

Example:

`git pull`

This helps keep my local project updated.

---

## Git Push

Push means uploading local commits to GitHub.

Example:

`git push`

This shares my local work online.

---

## Local and Remote Repositories

| Type              | Meaning                                  |
| ----------------- | ---------------------------------------- |
| Local Repository  | The Git repository on my computer        |
| Remote Repository | The online repository, usually on GitHub |

Developers usually work locally first, then push their changes to the remote repository.

---

## Simple Git Practice Workflow

1. Check changes
2. Stage files
3. Save a checkpoint
4. Upload to GitHub

Commands:

`git status`

`git add .`

`git commit -m "Update course notes"`

`git push`

---

## Easy Memory Notes

- `git status` = check changes
- `git diff` = what exactly these changes are (commits, branches, files)
- `git blame` = use to changes in speciic iles and check the date, time and who made the changes
- `git add .` = prepare files
- `git commit -m "message"` = save checkpoint
- `git push` = upload to GitHub
- `git pull` = get latest changes
- `git branch` = check branches
- `git merge` = combine branches
- `git clone` = copy repository

---

## Summary

Module 3 is about using Git practically.

The main idea is to understand how to move from editing files to saving changes with commits and sharing work through GitHub.

---

## Additional Resources

1. [Git: An Origin Story](https://www.linuxjournal.com/content/git-origin-story)
2. [Tech Talk: Linus Torvalds on git](https://www.youtube.com/watch?v=4XpnKHJAok8)
3. [Vim Cheatsheet](https://devhints.io/vim)
4. [Git patterns and anti-patterns for successful developers](https://youtu.be/t_4lLR6F_yk)
5. [Git Cheatsheet](https://education.github.com/git-cheat-sheet-education.pdf)
