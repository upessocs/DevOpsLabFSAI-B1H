Git Branching, Merging, and Rebasing
1. Creating Directories and Files
   Setting Up the Project Structure
   Create a new project directory:
   sh
   Copy
   Edit
   mkdir project
   cd project
   Inside the project, create a src directory:
   sh
   Copy
   Edit
   mkdir src
   Create essential files:
   sh
   Copy
   Edit
   touch README.md
   Create branch-specific files:
   sh
   Copy
   Edit
   touch z.txt  # Created in featureA branch
   touch x.txt  # Created in featureA branch
   touch s.txt  # Created in main branch
2. Working with Files
   Adding Content to Files
   Append text to README.md:
   sh
   Copy
   Edit
   echo "Hello World" >> README.md
   Append and display content:
   sh
   Copy
   Edit
   echo "content" >> README.md && cat README.md
   Output:
   css
   Copy
   Edit
   Hello World
   content
   Use echo with a newline:
   sh
   Copy
   Edit
   echo -e "hello \nme"
   Output:
   vbnet
   Copy
   Edit
   hello
   me
   Overwrite README.md:
   sh
   Copy
   Edit
   echo "Hello World 1" > README.md
3. Essential Git Commands
   Initializing and Checking Status
   Initialize a Git repository:
   sh
   Copy
   Edit
   git init
   Check remote repositories:
   sh
   Copy
   Edit
   git remote -v
   View the status of files:
   sh
   Copy
   Edit
   git status
   Stage all changes:
   sh
   Copy
   Edit
   git add .
   Commit staged changes:
   sh
   Copy
   Edit
   git commit -m "Initial commit"
   View commit history:
   sh
   Copy
   Edit
   git log
4. Branching and Switching
   Managing Branches
   List existing branches:
   sh
   Copy
   Edit
   git branch
   Rename the current branch to main:
   sh
   Copy
   Edit
   git branch -M main
   Create and switch to a new branch:
   sh
   Copy
   Edit
   git branch featureA
   git checkout featureA
   Create and switch to featureB in a single command:
   sh
   Copy
   Edit
   git checkout -b featureB
   Switch back to the main branch:
   sh
   Copy
   Edit
   git checkout main
5. Git Operations
   Reset, Merge, and Rebase
   Soft reset to a previous commit (keeps changes staged):
   sh
   Copy
   Edit
   git reset --soft <commit>
   Rebase featureA onto main:
   sh
   Copy
   Edit
   git rebase main
   Merge featureB into main:
   sh
   Copy
   Edit
   git merge featureB
   Hard reset to a specific commit (discards all changes):
   sh
   Copy
   Edit
   git reset --hard <commit>
   Squash commits from featureB into a single commit before merging:
   sh
   Copy
   Edit
   git merge --squash featureB
6. Final Content of Files
   File Contents After Operations
   README.md
   css
   Copy
   Edit
   Hello World 1
   content
   z.txt (Created in featureA branch)
   Initially empty but later added and committed.
   x.txt (Created in featureA branch)
   Initially empty but later added and committed.
   b.txt (Added in main branch)
   Committed with the message: "Added b.txt".
   s.txt (Added in main branch)
   Committed with the message: "s file added in main".