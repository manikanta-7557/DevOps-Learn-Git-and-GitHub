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

19. git push -u origin main --> This cmd is used to push the local commits to the remote repository for the first time.
    --> '-u' (***--set-upstream***) --> Links the local branch to the remote branch, so next time you can just use 'git push' without specifying origin main.

20. git push --> This cmd is used to push the local commits to the remote repository (***after the upstream is set with -u***).

21. git pull -u origin main --> This cmd is used to fetch and merge the remote repository changes to the local repository for the first time.
    --> '-u' (--set-upstream) --> Links the local branch to the remote branch, so next time you can just use 'git pull' without specifying origin main.
    --> **git pull origin main --rebase** --> This cmd is used to fetch the remote changes and replay the local commits on top of them instead of merging.
    --> '--rebase' --> Avoids creating an extra merge commit and keeps the commit history clean and linear.

    What is Rebase?
    Normally git pull does a merge which creates an extra merge commit, making history look messy.
    --rebase instead replays your local commits on top of the remote commits — keeping the history clean and linear.

    Visual difference:

    Without --rebase (merge):
    A --- B --- C (remote)
              \
               M (merge commit)
              /
    D --- E (your local commits)

    With --rebase:
    A --- B --- C --- D' --- E' (clean linear history)



22. git pull --> This cmd is used to fetch and merge the remote repository changes to the local repository (after the upstream is set with -u).

23. git remote -v --> This cmd is used to check the remote repository status.
    --> **'-v'** (--verbose) --> Shows extra details like the remote name along with its fetch and push URLs.

24. git stash --> This cmd is used to temporarily save the uncommitted changes and reset the working directory to a clean state.

25. git stash list --> This cmd is used to view all the stashed changes stored in the stash drawer.
    --> Output: stash@{0}: WIP on feature-branch: 41d3038 Initial Setup

26. git stash pop --> This cmd is used to restore the most recent stashed changes back to the working directory and deletes it from the stash list.

27. git stash apply --> This cmd is used to restore the most recent stashed changes back to the working directory but keeps a backup copy in the stash list.
    --> Difference between pop and apply:
        --> git stash pop   --> Restores + Deletes from stash list (most common).
        --> git stash apply --> Restores + Keeps a copy in stash list (useful to apply on different branches).

28. git stash drop --> This cmd is used to delete a specific stash from the stash list.
29. git stash clear --> This cmd is used to delete all the stashes from the stash list.

------------------------------------------------------------------------------------------
GitHub Tags
- In Git, Tags are references that point to specific points in your history
------------------------------------------------------------------------------------------
There are two types of Tags :
- Lightweight Tags : This type of tags just mention the **version details**.
- Annotated Tags : This type of tags give additional information like -> Tag Name, Creator Name, Date, Message.

**Commands Used** :
30. **git tag** --> This cmd is used to fetch all the tags that were given in the current repo.
31. **git tag <version_name_/_number>** --> This cmd helps us to give a tag name till a specific commit.
    --> **git tag -a <version_name_/_number> -m <"any message">** --> Annotated tag

32. git show <version_name_/_number> --> shows the details of the mentioned tag
33. git push origin <tag_name> --> Pushes the tag from the local repo to the remote repository.

***NOTE : **git push** command ignores tags and only transfers your code commits.*** 

34. git push origin main --tags --> This cmd is used to push all the local tags to the remote repository (including messy/broken/test tags).
    --> '--tags' --> Blindly pushes every single tag sitting on your local machine to GitHub.

35. git push origin main --follow-tags --> This cmd is used to push ***only*** the ***annotated tags*** that are directly attached to the commits being pushed.
    --> '--follow-tags' --> Prevents pushing unnecessary/broken tags and keeps the remote repository clean.
    --> Difference between --tags and --follow-tags:
        --> --tags        --> Pushes ALL local tags (messy + clean).
        --> --follow-tags --> Pushes ONLY annotated tags linked to the current commits being pushed.

------------------------------------------------------------------------------------------
Git Branch
------------------------------------------------------------------------------------------

36. git branch --> This cmd is used to list all the local branches (current branch is highlighted with *).

37. git branch <branchName> --> This cmd is used to create a new branch.

38. git checkout -b <branchName> --> This cmd is used to create a new branch and switch to it at the same time.

39. git switch -c <branchName> --> This cmd is used to create and switch to a new branch (modern alternative to checkout -b).

40. git switch <branchName> --> This cmd is used to switch to an existing branch (modern alternative to checkout).

41. git checkout <branchName> --> This cmd is used to switch to an existing branch.

42. git branch --all --> This cmd is used to list all branches (both local and remote).

43. git push origin <branchName> --> This cmd is used to push a specific branch to the remote repository.

44. git branch -m <oldName> <newName> --> This cmd is used to rename a branch.

45. git branch -d <branchName> --> This cmd is used to delete a branch (only if it is fully merged).
    --> git branch -D <branchName> --> Force deletes a branch even if it is not merged.

46. git push origin --delete <branchName> --> This cmd is used to delete a branch from the remote repository.

47. git log --graph --> This cmd is used to display the commit history in a visual graph format showing branches and merges.
    --> git log --graph --oneline --> Displays the graph in a compact single-line format.
