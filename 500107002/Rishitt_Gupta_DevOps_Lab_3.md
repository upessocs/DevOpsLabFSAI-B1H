# DevOps Lab 3
# GIT BASICS

## Using SSH and HTTP for Git
## Name: Rishitt Gupta  
**SAP ID:** 500107002  
**Enrollment Number:** R2142220352  
**Batch:** Full Stack AI B1 Hons  

---

### SSH Key Setup

Using SSH, we need both public and private keys to clone repositories securely.

#### 1. Generating SSH Key
```sh
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Verify the key:
```sh
ls ~/.ssh
```

#### 2. Reading the SSH Key
```sh
cat ~/.ssh/id_ed25519.pub
```

#### 3. Adding SSH Key to SSH-Agent
```sh
ssh-add ~/.ssh/id_ed25519
```

#### 4. Adding the Key to GitHub
- Go to **GitHub Settings → SSH and GPG keys → Add a new key**
- Copy and paste `id_ed25519.pub`

### Cloning Repository Using SSH
```sh
git clone git@github.com:username/repository.git
```

### Cloning Repository Using HTTP
```sh
git clone https://github.com/username/repository.git
```
Git will prompt for credentials if needed.

---

## Git Workflow

### 1. Initialize and Clone Repository
```sh
git init
git clone <repository-url>
```

### 2. Working on a Repository
1. Navigate to the repository.
2. Make changes.
3. Add changes:
   ```sh
   git add .
   ```
4. Commit changes:
   ```sh
   git commit -m "Your commit message"
   ```

### 3. Resolving Merge Conflicts
Always pull before pushing:
```sh
git pull origin main
git merge
git push origin main
```

---

## VIM Commands (for Git commit messages)
```sh
i → Insert mode
q → Quit
esc → Changing modes
shift + v → Visual mode
  - y → Copy / shift + insert
  - p → Paste
H, J, K, L → Move left, up, down, right
dd → Delete the line
u → Undo
/word → Search
esc + :wq → Save and quit
```
