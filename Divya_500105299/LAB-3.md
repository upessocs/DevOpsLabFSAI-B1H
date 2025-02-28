# **LAB-3**

**Name:** Divya Darshan Tiwari  
**SAP:** 500105299  
**Roll No.:** R2142220070  
**Batch:** B1H Full Stack AI

---

# **GIT BASICS**

## **Using SSH and HTTP for Git**

### **SSH Key Setup**

Using SSH ensures secure access to repositories with both public and private keys.

#### **1. Generating an SSH Key**

Run the following command to generate an SSH key:

```sh
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Verify if the key was generated at the default location:

```sh
ls ~/.ssh
```

#### **2. Viewing the SSH Key**

To display the public key:

```sh
cat ~/.ssh/id_ed25519.pub
```

#### **3. Adding the SSH Key to SSH-Agent**

```sh
ssh-add ~/.ssh/id_ed25519
```

#### **4. Adding the Key to GitHub**

- Go to **GitHub → Settings → SSH and GPG keys → Add a new key**
- Copy the contents of `id_ed25519.pub` and paste it into GitHub.

### **Cloning a Repository Using SSH**

```sh
git clone git@github.com:username/repository.git
```

---

### **Cloning a Repository Using HTTP**

```sh
git clone https://github.com/username/repository.git
```

If authentication is required, Git will prompt for your credentials.

---

## **Git Workflow**

### **1. Initialize and Clone a Repository**

```sh
git init
git clone <repository-url>
```

### **2. Working on a Repository**

1. Navigate to the repository.
2. Make necessary changes.
3. Stage changes:
   ```sh
   git add .
   ```
4. Commit changes with a message:
   ```sh
   git commit -m "Your commit message"
   ```

### **3. Resolving Merge Conflicts**

Before pushing changes, always pull the latest updates:

```sh
git pull origin main
git merge
```

Then push your changes:

```sh
git push origin main
```

---

## **VIM Commands (for Git Commit Messages)**

### **Basic Navigation & Editing**

- `i` → Insert mode
- `esc` → Change modes
- `q` → Quit
- `esc + :wq` → Save and quit

### **Text Manipulation**

- `dd` → Delete a line
- `u` → Undo last action
- `/something` → Search for "something"
- `shift + v` → Visual mode:
  - `y` → Copy
  - `p` → Paste

### **Movement Keys**

- `H` → Move left
- `L` → Move right
- `J` → Move down
- `K` → Move up

---
