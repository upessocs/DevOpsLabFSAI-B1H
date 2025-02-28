GIT BASICS
Using SSH and HTTP for Git
Git allows repositories to be accessed using either SSH or HTTP. While SSH provides a secure, password-less authentication method using key pairs, HTTP requires credentials for authentication.

SSH Key Setup
To securely interact with GitHub over SSH, both a public and private key are required.

1. Generating an SSH Key
   To generate an SSH key, execute:

sh
Copy
Edit
ssh-keygen -t ed25519 -C "your_email@example.com"
Verify that the key has been created in the default location:

sh
Copy
Edit
ls ~/.ssh
2. Reading the SSH Key
   To display the public key for adding it to GitHub:

sh
Copy
Edit
cat ~/.ssh/id_ed25519.pub
3. Adding SSH Key to SSH-Agent
   Before using the key, add it to the SSH agent:

sh
Copy
Edit
ssh-add ~/.ssh/id_ed25519
4. Adding the Key to GitHub
   Navigate to GitHub → Settings → SSH and GPG keys → Add a new key.
   Copy the contents of id_ed25519.pub.
   Paste the key into GitHub and save.
   Cloning Repositories
   Cloning Using SSH
   To clone a repository using SSH:

sh
Copy
Edit
git clone git@github.com:username/repository.git
Cloning Using HTTP
To clone a repository using HTTPS:

sh
Copy
Edit
git clone https://github.com/username/repository.git
If authentication is required, Git will prompt for credentials.
Git Workflow
1. Initialize and Clone a Repository
   To initialize a new repository:
   sh
   Copy
   Edit
   git init
   To clone an existing repository:
   sh
   Copy
   Edit
   git clone <repository-url>
2. Making Changes in a Repository
   Navigate to the repository.
   Modify files as needed.
   Add changes to the staging area:
   sh
   Copy
   Edit
   git add .
   Commit changes with a message:
   sh
   Copy
   Edit
   git commit -m "Your commit message"
3. Resolving Merge Conflicts
   Before pushing changes, always pull the latest updates:

sh
Copy
Edit
git pull origin main
git merge
Then, push changes:

sh
Copy
Edit
git push origin main
VIM Commands (For Git Commit Messages)
Basic Commands
i → Enter Insert mode
esc → Change modes
q → Quit
esc + :wq → Save and quit
Editing Commands
shift + v → Enter Visual mode
y → Copy
shift + insert → Paste
'H', 'J', 'K', 'L' → Move left, down, up, right
dd → Delete the current line
u → Undo the last action
/something → Search for "something"