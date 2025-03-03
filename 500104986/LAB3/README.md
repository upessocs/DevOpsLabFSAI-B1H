SSH Git (Lab3)

Git Basics
Using SSH and HTTP for Git
SSH Key Setup
Using SSH ensures secure access to Git repositories by utilizing both public and private keys.

1. Generating an SSH Key
Generate an SSH key by running the following command:

ssh-keygen -t ed25519 -C "ayush2004dey@gmail.com"
Verify the key is generated at the default location:

ls ~/.ssh
2. Viewing the SSH Key
To read the SSH key, use the following command:

cat ~/.ssh/id_ed25519.pub
3. Adding the SSH Key to the SSH-Agent
ssh-add ~/.ssh/id_ed25519
4. Adding the Key to GitHub
Navigate to GitHub Settings → SSH and GPG keys → Add a new key.
Copy and paste the contents of id_ed25519.pub.
Cloning a Repository Using SSH
git clone git@github.com:jahnaviichauhan/DemoMain.git
Cloning a Repository Using HTTP
git clone https://github.com/adx04/devopslab.git
When using HTTP, Git will prompt for your credentials if authentication is required.

Git Workflow
1. Initialize and Clone a Repository
git init
git clone <repository-url>
2. Working on a Repository
Navigate to the repository directory.
Make necessary changes.
Add changes to the staging area:
git add .
Commit changes with a descriptive message:
git commit -m "commit message"
3. Resolving Merge Conflicts
To avoid merge conflicts, always pull the latest changes before pushing:

git pull origin main
git merge
Push the changes to the repository:

git push origin main
VIM Commands (for Git commit messages)
1. i → Insert mode
2. q → Quit
3. esc → Changing modes
4. shift + v → Visual mode
   - y → Copy / shift + insert
   - p → Paste
5. u → Undo
6. ‘H’, ‘J’, ‘K’, ‘L’ → Move left, up, down, right
7. /something → Search something
8. dd → Delete the line
9. esc + :wq → Save and quit