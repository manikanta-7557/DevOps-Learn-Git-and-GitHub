1. **git init** --> Git Intialize
    --> git init -b master --> initializethe git with a branch name as 'master'.
2. git add <fileName> --> This cmd is used to add a specific file to the staging area.
    --> git add . --> The same above cmd but with an extension '.' helps to add all the documents (like * in java)
3. git status --> This cmd helps to check the status like what files are staged and what are not staged. (Comparing the Working directory files and staging dir/local repo).

4. git commit -m "message" --> This cmd is used to commit the staged files to the local repository with a message.

5. **git commit -a -m "message"** --> This cmd is used to commit the files directly to the local repository with a message (without staging*).

6. **git log** --> This cmd is used to display the commit history of the repository (shows commit ID, author, date, and message).
    --> git log --oneline --> Displays the commit history in a compact single-line format (short commit ID + message).
7. **git remote -v** --> This cmd is used to check the remote repository status (shows the remote name and its fetch/push URLs).
8. **git rm -rf <folder name>**
    - 'r' stands for **recursively** deletes all files and subdirectories inside a folder.
    - 'f' stands for **force** delete without asking for confirmation.
    Ex : rmdir /s /q <folder name>
9. **git diff** - Shows difference
    git diff --> This cmd is used to show the differences between the **working directory** and the **staging area** (unstaged changes).
    --> git diff --staged --> Shows the differences between the **staging area** and the **last commit** (staged changes).
    --> git diff <branch1> <branch2> --> Shows the differences between two branches.
    --> git diff <commitID1> <commitID2> --> Shows the differences between two commits.
10. **git rm --cached <filename>** --> To remove a file from the remote **GIT Repo** which is already commited.
10.1 **git rm <filename>** --> Remove the particular file from both - Local Repository & Remote Repository
11. **git restore --staged <filename>** --> To unstage the file from the staging area.
12. **git config --global --list** --> Shows the list of global variables with key & value
13. **git config --global user.name** --> This command shows the user name that is with the repository, similarly,
    **git config --global user.email** --> shows the email.

14. **git branch -M <branch name>** --> This cmd is used to change the currently pointing branch name.
15. **ssh-keygen -o** --> Inorder to generate an SSH Key to connect with the remote repository
    **cd %USERPROFILE%** --> To redirect to the user profile dir
    **dir /a** --> Shows all the directories within the directory (Even the hidden)
    **cd .ssh**
    **copy the id_xxxxxx.pub**
    **type id_xxxxxx.pub**
    **SSH id**

18. **git clone <repo URL>** --> This cmd is used to clone the remote repository to the local system.

