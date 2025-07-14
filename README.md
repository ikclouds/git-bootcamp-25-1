# Git and GitHub: A Foundation Guide to Learning

This study guide covers the foundational concepts and practical commands of Git and GitHub, essential for version control and collaborative software development.

## TOC

- [Git and GitHub: A Foundation Guide to Learning](#git-and-github-a-foundation-guide-to-learning)
  - [TOC](#toc)
  - [Additional resources](#additional-resources)
  - [I. Short Answer Quiz](#i-short-answer-quiz)
  - [II. Quiz Answer Key](#ii-quiz-answer-key)
  - [III. Essay Format Questions](#iii-essay-format-questions)
  - [IV. Glossary of Key Terms](#iv-glossary-of-key-terms)
  - [Guide](#guide)
    - [Git basics](#git-basics)
      - [Purpose and Benefits of Git](#purpose-and-benefits-of-git)
      - [Git Installation and Verification](#git-installation-and-verification)
      - [Core Git Concepts](#core-git-concepts)
      - [Git and GitHub](#git-and-github)
    - [Upstream vs. Origin](#upstream-vs-origin)
      - [Basic Git Workflow and Commands](#basic-git-workflow-and-commands)
      - [Branches](#branches)
      - [Merging Branches (`git merge`)](#merging-branches-git-merge)
      - [Purpose of an Upstream Branch](#purpose-of-an-upstream-branch)
      - [How to Set Upstream](#how-to-set-upstream)
      - [Pushing Changes to Origin After Merging from Upstream](#pushing-changes-to-origin-after-merging-from-upstream)
    - [Basic Git Commands](#basic-git-commands)
      - [git init](#git-init)
      - [git clone](#git-clone)
      - [git status](#git-status)
      - [git add](#git-add)
      - [git commit](#git-commit)
      - [git log](#git-log)
      - [git branch](#git-branch)
      - [git checkout](#git-checkout)
      - [git merge](#git-merge)
      - [git pull](#git-pull)
      - [git push](#git-push)
      - [git remote](#git-remote)
      - [git fetch](#git-fetch)
      - [git reset](#git-reset)
      - [git stash](#git-stash)
      - [git diff](#git-diff)
    - [Git Aliases](#git-aliases)
      - [Setting Up Git Aliases](#setting-up-git-aliases)
      - [Commonly Used Git Aliases](#commonly-used-git-aliases)
        - [Basic Command Shortcuts](#basic-command-shortcuts)
        - [Enhanced Log Commands](#enhanced-log-commands)
        - [Workflow Enhancers](#workflow-enhancers)
        - [Branch Management](#branch-management)
      - [Viewing Your Aliases](#viewing-your-aliases)
      - [Removing Aliases](#removing-aliases)

## Additional resources

- [Markdown Guide: Basic Syntax](https://www.markdownguide.org/basic-syntax/)

## I. Short Answer Quiz

Answer each question in 2-3 sentences.

1. What is the primary purpose of Git, and in what scenarios is it most beneficial?
2. How can you verify that Git is correctly installed on your computer after following the installation steps?
3. Explain the significance of the .git folder within a project directory.
4. Describe the function of the git status command.
5. What is the difference between `git add .` and `git add filename`?
6. What is a "commit" in Git, and why are commit messages important?
7. Explain the concept of "branches" in Git and their purpose in a collaborative development workflow.
8. How do you switch between different branches in Git? Provide a command example.
9. What is the purpose of a .gitignore file, and what types of files would you typically include in it?
10. Briefly explain the role of GitHub in relation to Git, and how they interact.

## II. Quiz Answer Key

1. **What is the primary purpose of Git, and in what scenarios is it most beneficial?** Git is a version control system used to track changes in source code and other files during software development. It is most beneficial in team environments where multiple developers work on the same project, as it helps manage conflicts, track historical changes, and allows for parallel development without interference.
2. **How can you verify that Git is correctly installed on your computer after following the installation steps?** To verify Git installation, open your terminal or command prompt and type git --version. If Git is installed correctly, it will display the current version number, indicating it's ready for use.
3. **Explain the significance of the .git folder within a project directory.** The .git folder is a hidden system folder created upon Git initialization. It stores all the necessary technical information for Git to track changes, manage versions, and maintain the repository's history, acting as the core of the Git repository.
4. **Describe the function of the `git status` command.** The `git status command` provides information about the current state of the Git repository. It shows which branch you are on, which files have been modified, which are staged for the next commit, and which are untracked.
5. **What is the difference between `git add .` and `git add filename`?** `git add filename` stages a specific file for the next commit, meaning only changes in that particular file will be included. In contrast, `git add .` stages all new and modified files in the current directory and its subdirectories, preparing them all for the next commit.
6. **What is a "commit" in Git, and why are commit messages important?** A commit is a snapshot of your project at a specific point in time, saving changes to the repository's history. Commit messages are crucial because they provide a clear and concise description of the changes made in that commit, aiding in understanding the project's evolution and facilitating collaboration.
7. **Explain the concept of "branches" in Git and their purpose in a collaborative development workflow.** Branches in Git represent independent lines of development. They allow developers to work on new features or bug fixes without affecting the main codebase, enabling parallel workstreams and ensuring the stability of the primary project version until changes are ready to be integrated.
8. **How do you switch between different branches in Git? Provide a command example.** To switch between branches, you use the git checkout command followed by the branch name. For example, to switch to a branch named "feature-x", you would type git checkout feature-x.
9. **What is the purpose of a `.gitignore` file, and what types of files would you typically include in it?** A `.gitignore` file specifies intentionally untracked files and directories that Git should ignore. You would typically include local configuration files, build artifacts, temporary files, personal log files, and sensitive information in `.gitignore` to prevent them from being committed to the repository.
10. **Briefly explain the role of GitHub in relation to Git, and how they interact.** Git is a local version control system, while GitHub is a web-based platform that provides remote hosting for Git repositories. GitHub acts as a centralized hub for collaborative development, allowing developers to share their local Git repositories, track team contributions, manage issues, and review code remotely.

## III. Essay Format Questions

1. Discuss the advantages of using Git for version control in a large-scale software project involving multiple developers. Provide specific examples of how Git's features (e.g., branching, merging, commit history) facilitate collaboration and maintain code integrity.
2. Elaborate on the workflow of making changes in a Git repository from initial modification to pushing to a remote server. Include detailed steps for staging, committing, and pushing, and explain the significance of each step.
3. Compare and contrast the git checkout command used for switching branches versus the git checkout -b command for creating and switching to a new branch. Discuss scenarios where each would be more appropriate.
4. Explain the process of integrating changes from one branch into another using git merge. Describe potential conflicts that might arise during a merge and how Git helps in resolving them.
5. Describe the steps involved in connecting a local Git repository to a remote GitHub repository. Explain the purpose of `git remote add origin` and `git push -u origin <branch-name>` in this process, and discuss how git pull is used to synchronize local and remote repositories.

## IV. Glossary of Key Terms

1. **Git**: A distributed version control system for tracking changes in source code during software development.
2. **GitHub**: A web-based platform for version control and collaboration, providing hosting for Git repositories.
3. **Repository (Repo)**: A storage location where all the files for a project, along with their revision history, are kept.
4. **Version Control System (VCS)**: A system that records changes to a file or set of files over time so that you can recall specific versions later.
5. **Initialize (Git Init)**: The process of creating a new Git repository in a project directory using git init, which creates the hidden .git folder.
6. **Terminal/Console**: A command-line interface used to interact with the operating system and run Git commands.
7. **git --version**: A command used to check the installed version of Git.
8. **git --help**: A command that displays a list of common Git commands and options.
9. **git status**: A command that shows the current state of the working directory and the staging area, indicating which files are tracked, untracked, modified, or staged.
10. **Untracked Files**: Files in your working directory that Git is not currently monitoring.
11. **Staging Area (Index)**: An intermediate area where changes are prepared before being committed to the repository.
12. **git add <filename>**: A command to add a specific file to the staging area.
13. **git add .**: A command to add all new and modified files in the current directory and its subdirectories to the staging area.
14. **Commit**: A snapshot of your repository at a specific point in time. It records changes that have been staged.
15. **git commit -m "message"**: A command to save staged changes to the repository with a descriptive message.
16. **Commit Hash**: A unique identifier (a hexadecimal string) assigned to each commit, allowing you to refer to specific versions of your project.
17. **Branch**: An independent line of development within a Git repository. It allows developers to work on new features without affecting the main codebase.
18. **git branch**: A command to list existing branches in the repository, with the current branch highlighted.
19. **git branch <branch-name>**: A command to create a new branch.
20. **git checkout <branch-name>**: A command to switch from the current branch to another existing branch.
21. **git checkout -b <new-branch-name>**: A command to create a new branch and immediately switch to it.
22. **git branch -d <branch-name>**: A command to delete a specified branch.
23. **.gitignore**: A special file that tells Git which files or directories to ignore and not track.
24. **git merge <branch-name>**: A command used to integrate changes from a specified branch into the current branch.
25. **Remote Repository**: A version of your repository hosted on the internet or a network, accessible by multiple collaborators (e.g., on GitHub).
26. **git config --global user.name "Your Name"**: A command to set your global Git username for commits.
27. **git config --global user.email "<your.email@example.com>"**: A command to set your global Git email for commits.
28. **git remote add origin <URL>**: A command to add a new remote repository, typically named "origin," with a specified URL.
29. **git push -u origin <branch-name>**: A command to push local commits to a remote repository for the first time, setting the upstream tracking branch.
30. **git push**: A command to send committed changes from your local repository to the remote repository.
31. **git clone <URL>**: A command to create a local copy of an existing remote repository.
32. **git pull**: A command to fetch and integrate (download) changes from a remote repository into your current local branch.

## Guide

---

### Git basics

Git is a fundamental technology for **version control**. It is a **distributed version control system** (VCS) used to **track changes in source code and other files** during software development.

#### Purpose and Benefits of Git

The **primary purpose of Git** is to serve as a version control system. While it can be used by individuals working on a single project, Git is **most beneficial in team environments** where multiple developers collaborate on the same project. In such scenarios, Git helps to:

- **Manage conflicts** that arise when multiple developers make changes.
- **Track historical changes** to files and projects.
- **Allow for parallel development** without interference.
- **Enable developers to work on new features or bug fixes without affecting the main codebase**.
- **Ensure the stability of the primary project version** until changes are ready to be integrated.
For large projects, such as websites like VKontakte or YouTube, Git ensures that erroneous changes do not crash the system, maintaining different versions like production, tested, and development versions.

#### Git Installation and Verification

Git is not installed by default on most computers. To use Git, you need to download and install it from the official website (e.g., git-scm.com). After following the installation steps, you can **verify that Git is correctly installed** by opening your terminal or command prompt and typing `git --version`. If installed correctly, it will display the current version number, indicating it's ready for use. Another helpful command is `git --help`, which displays a list of common Git commands and options.

#### Core Git Concepts

- **Repository (Repo):** A storage location where all the files for a project, along with their revision history, are kept.

- **.git Folder:** When a new Git repository is initialized in a project directory using the `git init` command, a **hidden system folder called `.git`** is created. This folder is crucial because it **stores all the necessary technical information for Git to track changes, manage versions, and maintain the repository's history**, acting as the core of the Git repository. It contains various subfolders and files that record technical data, though detailed knowledge of its internal structure is typically not required for basic use.
- **Terminal/Console:** This is the **command-line interface** used to interact with the operating system and run Git commands.

#### Git and GitHub

**Git is a local version control system**, meaning it operates on your computer. **GitHub, on the other hand, is a web-based platform that provides remote hosting for Git repositories**. It acts as a **centralized hub for collaborative development**, allowing developers to:

- Share their local Git repositories with others.
- Track team contributions.
- Manage issues.
- Review code remotely.
- Visually display what's happening locally.

**Connecting a Local Repository to a Remote GitHub Repository:**

1. **Configure User Identity:** Set your global Git username and email using `git config --global user.name "Your Name"` and `git config --global user.email "your.email@example.com"`. These details will be associated with your commits.
2. **Create Remote Repository on GitHub:** On GitHub, you create a new repository.
3. **Add Remote Origin (`git remote add origin`):** Use the `git remote add origin <URL>` command to **add a new remote repository**, typically named "origin," with a specified URL. This links your local repository to the remote one.
4. **Push Initial Commits (`git push -u origin <branch-name>`):** To send your local commits to the remote repository for the first time, you use `git push -u origin <branch-name>`. The `-u` flag sets the upstream tracking branch, meaning subsequent `git push` commands can be shorter.
5. **Push Subsequent Changes (`git push`):** After the initial push, you can use `git push` to send committed changes from your local repository to the remote.

**Synchronizing with Remote Repositories:**

- **Cloning (`git clone`):** To get a local copy of an existing remote repository, you use `git clone <URL>`. This downloads the entire project history and sets up the remote tracking.
- **Pulling (`git pull`):** The `git pull` command is used to **fetch and integrate (download) changes from a remote repository into your current local branch**. It's essential to use `git pull` before starting work to ensure your local repository is up-to-date with any changes made by other collaborators.

### Upstream vs. Origin

In Git, **"upstream"** generally refers to the **main or original repository and its branches from which you've copied code or where your changes will eventually be pushed.** It represents the source of truth or the central point of collaboration for a project.

Here's a breakdown of what that means and why it's important:

- **Origin**: When you clone a repository (`git clone`), Git automatically sets up a remote named `origin`. This typically points to **your own fork** of a project or the repository you initially cloned. You usually push your local changes to `origin`.
- **Upstream**: When you're contributing to an open-source project, you'll often **fork** the original repository to your own GitHub/GitLab account. In this scenario, your fork is `origin`, and the **original project's repository is typically referred to as `upstream`**. This allows you to:
  - **Fetch updates** from the original project to keep your local copy in sync with the latest changes (`git fetch upstream`).
  - **Propose your changes** back to the original project via pull requests.

#### Basic Git Workflow and Commands

The Git workflow involves a series of steps to manage changes in your project:

1. **`git status` Command:** This command is frequently used to **provide information about the current state of the Git repository**. It shows:
    - Which branch you are currently on.
    - Which files have been modified.
    - Which files are staged for the next commit.
    - Which files are untracked.
2. **Staging Changes (`git add`):** Before changes can be committed (saved), they must be moved to the **staging area (or index)**. This is an intermediate area where changes are prepared.
    - **`git add <filename>`:** This command **stages a specific file** for the next commit, meaning only changes in that particular file will be included.
    - **`git add .`:** This command **stages all new and modified files** in the current directory and its subdirectories, preparing them all for the next commit.
3. **Committing Changes (`git commit`):** A **commit is a snapshot of your project at a specific point in time**, saving the staged changes to the repository's history.
    - **Commit Messages:** **Commit messages are crucial** because they provide a clear and concise description of the changes made in that commit, aiding in understanding the project's evolution and facilitating collaboration. A common command format is `git commit -m "message"`.
    - **Commit Hash:** Each commit is assigned a **unique identifier**, a hexadecimal string known as a commit hash, which allows you to refer to specific versions of your project. The more frequently you commit, the more opportunities you have to return to a specific stage of your application's development.
4. **Ignoring Files (`.gitignore`):** A **`.gitignore` file** is a special file that tells Git which files or directories to intentionally untrack and ignore. You would typically include files like **local configuration files, build artifacts, temporary files, personal log files, and sensitive information** in `.gitignore` to prevent them from being committed to the repository. The `.gitignore` file itself needs to be added and committed so Git knows about its contents.

#### Branches

**Branches in Git represent independent lines of development**. Their purpose is to allow developers to **work on new features or bug fixes without affecting the main codebase**, enabling parallel workstreams and ensuring the stability of the primary project version until changes are ready to be integrated.

- **`git branch`:** This command is used to **list existing branches** in the repository, with the current branch highlighted.
- **`git branch <branch-name>`:** Creates a **new branch**.
- **`git checkout <branch-name>`:** Used to **switch from the current branch to another existing branch**. When switching branches, the files in your working directory will reflect the version of the project on that branch.
- **`git checkout -b <new-branch-name>`:** This command allows you to **create a new branch and immediately switch to it**. This is a quicker way to set up a new development line.
- **`git branch -d <branch-name>`:** Used to **delete a specified branch**.

#### Merging Branches (`git merge`)

The `git merge <branch-name>` command is used to **integrate changes from a specified branch into the current branch**. For example, if you are on the `master` branch and want to incorporate changes from a `readme` branch, you would use `git merge readme`. This combines the development histories of the two branches. Git helps in resolving potential conflicts that might arise during a merge.

#### Purpose of an Upstream Branch

The primary purpose of an upstream branch is to establish a **tracking relationship** between your local branch and a remote branch. This relationship offers several benefits:

- **Simplified `git pull` and `git push`**: Once an upstream is set for your local branch, you can simply use `git pull` and `git push` without specifying the remote or branch name. Git automatically knows where to fetch from and push to.
- **Tracking progress**: Git can tell you if your local branch is **"ahead"** (has commits not yet pushed to the upstream) or **"behind"** (is missing commits from the upstream) its remote counterpart. This helps you stay informed about the synchronization status of your branches.
- **Facilitates collaboration**: It creates a clear path for integrating changes from the main project into your local work and for submitting your contributions back to the main project.

#### How to Set Upstream

You can set the upstream for a local branch using one of these common methods:

- **When first pushing a new branch**:

    ```bash
    git push -u origin <your-branch-name>
    ```

    The `-u` (or `--set-upstream`) flag tells Git to set the specified remote branch (`origin/<your-branch-name>` in this case) as the upstream for your local branch.

- **For an existing local branch**:

    ```bash
    git branch --set-upstream-to=origin/<remote-branch-name> <local-branch-name>
    ```

    If you omit `<local-branch-name>`, it defaults to your currently checked-out branch.

- **Adding a new remote named `upstream` (common in forking workflows)**:

    ```bash
    git remote add upstream https://github.com/ORIGINAL-OWNER/ORIGINAL-REPOSITORY.git
    ```

    After this, you can `git fetch upstream` to get updates from the original repository.

#### Pushing Changes to Origin After Merging from Upstream

The command `git push origin <branch-name>` specifically pushes your current branch to the corresponding branch in your fork.

```bash
git push origin <branch-name>
```

This is the standard command for pushing your local changes to your fork (origin) after you've merged updates from the upstream repository.

In a typical fork workflow:

1. You fork a repository on GitHub (or another platform)
2. The original repository is set up as "upstream"
3. Your fork is set up as "origin"
4. You periodically fetch and merge changes from upstream
5. After merging those changes locally, you need to update your fork

### Basic Git Commands

#### git init

Initializes a new Git repository in the current directory, creating the hidden `.git` folder that tracks all changes.

```bash
# Create a new Git repository
git init

# Output
Initialized empty Git repository in /path/to/your/project/.git/
```

#### git clone

Creates a copy of a remote repository on your local machine, including all files, branches, and commit history.

```bash
# Clone a repository from GitHub
git clone https://github.com/username/repository.git

# Clone to a specific folder
git clone https://github.com/username/repository.git my-project-folder
```

#### git status

Shows the current state of your working directory - which files are modified, staged, or untracked.

```bash
git status

# Output example
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        new-file.txt
```

#### git add

Adds file changes to the staging area, preparing them for the next commit.

```bash
# Add a specific file
git add filename.txt

# Add all modified and new files
git add .

# Add specific file types
git add *.js
```

#### git commit

Records the changes in the repository's history with a descriptive message.

```bash
# Commit with a message
git commit -m "Add login functionality"

# Commit all modified tracked files without staging
git commit -am "Fix typos in documentation"
```

#### git log

Displays the commit history, showing commit hashes, authors, dates, and messages.

```bash
# View commit history
git log

# Show simplified one-line history
git log --oneline

# Show graphical representation of branch history
git log --graph --oneline --all
```

#### git branch

Lists, creates, or deletes branches in your repository.

```bash
# List all local branches (* marks current branch)
git branch

# Create a new branch
git branch feature-login

# Delete a branch
git branch -d feature-login

# List remote branches
git branch -r
```

#### git checkout

Switches between branches or restores files from a specific commit.

```bash
# Switch to an existing branch
git checkout develop

# Create and switch to a new branch
git checkout -b feature-navbar

# Discard changes in a file
git checkout -- filename.txt
```

#### git merge

Combines changes from different branches together.

```bash
# Merge a branch into your current branch
git checkout main
git merge feature-login
```

#### git pull

Fetches changes from a remote repository and integrates them into your current branch.

```bash
# Pull changes from origin remote
git pull origin main

# Pull with rebase instead of merge
git pull --rebase origin main
```

#### git push

Uploads local repository changes to the remote repository.

```bash
# Push changes to remote
git push origin main

# Push and set upstream branch
git push -u origin feature-search
```

#### git remote

Manages the set of remote repositories you're tracking.

```bash
# View remote repositories
git remote -v

# Add a new remote
git remote add upstream https://github.com/original-owner/original-repo.git

# Remove a remote
git remote remove upstream
```

#### git fetch

Downloads objects and refs from a remote repository without merging.

```bash
# Fetch from origin
git fetch origin

# Fetch from all remotes
git fetch --all
```

#### git reset

Resets the current HEAD to the specified state, with different modes affecting staging area and working directory.

```bash
# Unstage files but keep changes
git reset HEAD filename.txt

# Reset to a specific commit, preserving changes as unstaged
git reset a1b2c3d4

# Hard reset to a specific commit (discards all changes)
git reset --hard a1b2c3d4
```

#### git stash

Temporarily saves changes that you don't want to commit immediately.

```bash
# Stash current changes
git stash

# List stashes
git stash list

# Apply most recent stash
git stash apply

# Apply specific stash
git stash apply stash@{2}

# Remove most recent stash after applying
git stash pop
```

#### git diff

Shows changes between commits, commit and working tree, etc.

```bash
# Show unstaged changes
git diff

# Show staged changes
git diff --staged

# Compare two branches
git diff main..feature-branch
```

### Git Aliases

Git aliases allow you to create shortcuts for frequently used Git commands. They save time and improve productivity by reducing the amount of typing needed for common operations.

#### Setting Up Git Aliases

Git aliases are created using the `git config` command with the `--global` flag to make them available across all your repositories.

```bash
git config --global alias.<shortcut> '<command>'
```

#### Commonly Used Git Aliases

Here are some useful Git aliases that many developers incorporate into their workflow:

##### Basic Command Shortcuts

```bash
# Create shorter versions of common commands
git config --global alias.co 'checkout'
git config --global alias.br 'branch'
git config --global alias.ci 'commit'
git config --global alias.st 'status'
git config --global alias.unstage 'reset HEAD --'
```

Usage examples:

```bash
git co main        # Instead of git checkout main
git br -a          # Instead of git branch -a
git ci -m "Fix bug" # Instead of git commit -m "Fix bug"
git st             # Instead of git status
git unstage file.txt # Instead of git reset HEAD -- file.txt
```

##### Enhanced Log Commands

```bash
# One-line log with decorations showing branches and tags
git config --global alias.lg 'log --graph --pretty=format:"%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset" --abbrev-commit'

# Show last commit
git config --global alias.last 'log -1 HEAD'

# Show all commits as a simplified tree
git config --global alias.tree 'log --graph --oneline --all'
```

Usage examples:

```bash
git lg             # Shows decorated commit history
git last           # Shows details of the most recent commit
git tree           # Shows a graphical representation of all branches
```

##### Workflow Enhancers

```bash
# Show changes in a compact way
git config --global alias.df 'diff --color --color-words --abbrev'

# Amend the previous commit without changing the commit message
git config --global alias.amend 'commit --amend --no-edit'

# Show all configured aliases
git config --global alias.aliases '!git config --get-regexp alias'

# Undo the last commit but keep changes
git config --global alias.undo 'reset --soft HEAD~1'
```

Usage examples:

```bash
git df             # Shows colorized word-by-word diff
git amend          # Updates the last commit with staged changes
git aliases        # Lists all your configured Git aliases
git undo           # Undoes the last commit while preserving changes
```

##### Branch Management

```bash
# Clean up local branches that have been merged
git config --global alias.cleanup '!git branch --merged | grep -v "\*" | xargs -n 1 git branch -d'

# Show all branches with last commit date
git config --global alias.recent 'for-each-ref --sort=-committerdate --format="%(committerdate:short) %(refname:short)" refs/heads/'
```

Usage examples:

```bash
git cleanup        # Removes merged branches
git recent         # Shows branches sorted by latest commit
```

#### Viewing Your Aliases

To see all configured aliases:

```bash
git config --list | grep alias
# or if you set the 'aliases' alias above
git aliases
```

#### Removing Aliases

To remove an alias:

```bash
git config --global --unset alias.<shortcut>
```

Example:

```bash
git config --global --unset alias.co  # Removes the 'co' alias
```
