# Quiz Notes — Version Control 🔄

This file contains quiz questions, answers, and explanations from the **Version Control** course in the Meta Full-Stack Development learning path.

---

# Module 1: Software Collaboration

## 🟦 Question 1

**What type of system uses a server and client for version control?**

### 🟩 Answer

**Centralized Version Control System, CVCS**

A Centralized Version Control System uses a central server that stores the main repository, while users work from client machines.

---

## 🟦 Question 2

**What requirement of centralized version control systems contributes to their slower performance?**

### 🟩 Answer

**Most operations require communication with the central server.**

Because the client often needs to connect to the central server, actions can be slower compared to distributed systems.

---

## 🟦 Question 3

**What type of version control system is described as faster than its centralized counterpart?**

### 🟩 Answer

**Distributed Version Control System, DVCS**

A DVCS is usually faster because each user has a full local copy of the repository and can perform many actions locally.

---

## 🟦 Question 4

**In a DVCS, what action must you take to view the latest changes from others?**

### 🟩 Answer

**Pull the latest changes from the remote repository.**

Command:

`git pull`

---

## 🟦 Question 5

**In a CVCS, what does the main repository on the server contain?**

### 🟩 Answer

**The complete project history and the main version of the codebase.**

In a Centralized Version Control System, the central server stores the main repository that all users depend on.

---

## 🟦 Question 6

**In a DVCS, what does each user essentially function as?**

### 🟩 Answer

**Each user functions as their own repository/server copy.**

In a Distributed Version Control System, every user has a full local copy of the project history.

---

## 🟦 Question 7

**What specific issue arises in a shared code base as more developers contribute changes?**

### 🟩 Answer

**Merge conflicts.**

Merge conflicts can happen when multiple developers change the same file or the same lines of code.

---

## 🟦 Question 8

**In a DVCS workflow, when must you connect to the server to share your work?**

### 🟩 Answer

**When pushing or pulling changes.**

A developer can commit locally without connecting to the server, but a connection is needed when sharing work or getting updates from others.

Commands:

`git push`

`git pull`

---

## 🟦 Question 9

**In a CVCS, what is required for most client operations?**

### 🟩 Answer

**A connection to the central server.**

In a CVCS, most actions depend on the central repository, so users usually need server access.

---

## 🟦 Question 10

**Git was developed by Linus Torvalds to host the Linux kernel’s source code. Is this statement fully accurate?**

### 🟩 Answer

**Not fully accurate.**

Better version:

**Git was created by Linus Torvalds in 2005 to manage the Linux kernel source code efficiently as a fast, distributed version control system.**

Git is a version control system.  
GitHub is a hosting platform.

---

## 🟦 Question 11

**Which of the following are centralized Version Control Systems? Select all that apply.**

Options:

- Concurrent Versions System
- Mercurial
- Subversion
- Git

### 🟩 Answer

- ✅ Concurrent Versions System
- ✅ Subversion
- ❌ Mercurial
- ❌ Git

**Explanation:**

CVS and Subversion are centralized version control systems.  
Git and Mercurial are distributed version control systems.

---

## 🟦 Question 12

**Which of the following complements Version Control during software development? Select all that apply.**

Options:

- Continuous Integration
- Continuous Delivery
- Continuous Deployment

### 🟩 Answer

- ✅ Continuous Integration
- ✅ Continuous Delivery
- ✅ Continuous Deployment

**Explanation:**

These practices complement version control because they help teams automatically build, test, deliver, or deploy code after changes are committed.

---

# Module 2: Command Line

## 🟦 Question 13

**What is the command line?**

### 🟩 Answer

**The command line is a text-based interface used to interact with the computer by typing commands.**

It allows developers to navigate folders, create files, run programs, install tools, and use Git.

---

## 🟦 Question 14

**Why is the command line important for developers?**

### 🟩 Answer

**The command line is important because many development tools, including Git, are commonly used through terminal commands.**

It helps developers work faster and gives more control over projects.

---

## 🟦 Question 15

**Which command is used to move into a folder?**

### 🟩 Answer

`cd folder-name`

Example:

`cd Documents`

---

## 🟦 Question 16

**Which command is used to move back one folder?**

### 🟩 Answer

`cd ..`

This command moves from the current folder to the parent folder.

---

## 🟦 Question 17

**Which command is used to create a new folder?**

### 🟩 Answer

`mkdir folder-name`

Example:

`mkdir version-control-practice`

---

## 🟦 Question 18

**Which command lists files and folders on Windows?**

### 🟩 Answer

`dir`

This command displays the files and folders in the current directory on Windows.

---

## 🟦 Question 19

**Which command lists files and folders on macOS or Linux?**

### 🟩 Answer

`ls`

This command displays the files and folders in the current directory on macOS or Linux.

---

# Module 3: Work with Git

## 🟦 Question 20

**What is Git?**

### 🟩 Answer

**Git is a distributed version control system used to track changes in files and code.**

It helps developers save project history, collaborate with others, create branches, and recover earlier versions.

---

## 🟦 Question 21

**What is a repository?**

### 🟩 Answer

**A repository is a project folder tracked by Git.**

It contains the project files and the history of changes.

---

## 🟦 Question 22

**Which command starts a new Git repository?**

### 🟩 Answer

`git init`

This command initializes a new Git repository in the current folder.

---

## 🟦 Question 23

**Which command shows the current state of the project?**

### 🟩 Answer

`git status`

This command shows changed files, untracked files, and staged files.

---

## 🟦 Question 24

**Which command stages all changed files?**

### 🟩 Answer

`git add .`

This command adds all changed files to the staging area.

---

## 🟦 Question 25

**Which command saves a checkpoint in Git?**

### 🟩 Answer

`git commit -m "message"`

Example:

`git commit -m "Add version control notes"`

A commit saves a version of the project with a message.

---

## 🟦 Question 26

**What is a commit?**

### 🟩 Answer

**A commit is a saved checkpoint of the project.**

Each commit records a version of the project at a specific time.

---

## 🟦 Question 27

**What is a branch?**

### 🟩 Answer

**A branch is a separate workspace for changes.**

Branches allow developers to work on new features or fixes without changing the main project immediately.

---

## 🟦 Question 28

**Which command creates and switches to a new branch?**

### 🟩 Answer

`git checkout -b branch-name`

Example:

`git checkout -b login-page`

---

## 🟦 Question 29

**What does `git merge` do?**

### 🟩 Answer

`git merge` combines changes from one branch into another branch.

Example:

`git merge login-page`

---

## 🟦 Question 30

**What does `git push` do?**

### 🟩 Answer

`git push` uploads local commits to a remote repository such as GitHub.

---

## 🟦 Question 31

**What does `git pull` do?**

### 🟩 Answer

`git pull` downloads the latest changes from the remote repository.

It helps keep the local project updated.

---

## 🟦 Question 32

**What does `git clone` do?**

### 🟩 Answer

`git clone` copies a remote repository from GitHub to the computer.

Example:

`git clone repository-url`

---

## 🟦 Question 33

**What is the difference between a local repository and a remote repository?**

### 🟩 Answer

| Type              | Meaning                                         |
| ----------------- | ----------------------------------------------- |
| Local Repository  | The Git repository on my computer               |
| Remote Repository | The online repository, usually hosted on GitHub |

Developers work locally first, then push changes to the remote repository.

---

## 🟦 Question 34

**What is the staging area?**

### 🟩 Answer

**The staging area is where files are prepared before committing.**

Files must be added to the staging area before they are saved in a commit.

---

## 🟦 Question 35

**What is the basic Git workflow?**

### 🟩 Answer

1. Edit files
2. Check status
3. Add files
4. Commit changes
5. Push to GitHub

Commands:

`git status`

`git add .`

`git commit -m "Update project"`

`git push`

---

# Key Memory Notes

- CVCS = one central server
- DVCS = everyone has a full copy
- Git = version control system
- GitHub = online repository hosting platform
- Repository = tracked project folder
- Commit = saved checkpoint
- Branch = safe workspace
- Merge = combine changes
- Push = upload changes
- Pull = get latest changes
- Clone = copy repository
- Conflict = Git needs human decision
