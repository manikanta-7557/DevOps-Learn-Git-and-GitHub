1. **git init** --> Git Intialize
    --> git init -b master --> initializethe git with a branch name as 'master'.
2. git add <fileName> --> This cmd is used to add a specific file to the staging area.
    --> git add . --> The same above cmd but with an extension '.' helps to add all the documents (like * in java)
3. git status --> This cmd helps to check the status like what files are staged and what are not staged. (Comparing the Working directory files and staging dir/local repo).

4. git commit -m "message" --> This cmd is used to commit the staged files to the local repository with a message.

5. git commit -a -m "message" --> This cmd is used to commit the files directly to the local repository with a message (without staging*).

6. git log --> This cmd is used to display the commit history of the repository (shows commit ID, author, date, and message).
    --> git log --oneline --> Displays the commit history in a compact single-line format (short commit ID + message).
