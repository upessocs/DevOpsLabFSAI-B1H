# DevOps Lab 3: Git Basics  

## Using SSH and HTTP for Git  

## Details  
**Name:** Rishitt Gupta  
**SAP ID:** 500107002  
**Enrollment Number:** R2142220352  
**Batch:** Full Stack AI B1 Hons  

---  

## SSH Key Setup  

### 1. Generate SSH Key  
```
ssh-keygen -t ed25519 -C "rishittg7@gmail.com"
```  
Verify the key:  
```
ls ~/.ssh
```  

### 2. Read the SSH Key  
```
cat ~/.ssh/id_ed25519.pub
```  

### 3. Add SSH Key to SSH-Agent  
```
ssh-add ~/.ssh/id_ed25519
```  

### 4. Add the Key to GitHub  
- Go to **GitHub Settings → SSH and GPG keys → Add a new key**  
- Copy and paste `id_ed25519.pub`  

## Clone Repository  

### Using SSH  
```
git clone git@github.com:rishuu42/repository.git
```  

### Using HTTP  
```
git clone https://github.com/rishuu42/repository.git
```  

---  

## Git Workflow  

### 1. Initialize and Clone  
```
git init  
git clone <repository-url>
```  

### 2. Work on Repository  
1. Navigate to the repository.  
2. Make changes.  
3. Add changes:  
   ```
   git add .
   ```  
4. Commit changes:  
   ```
   git commit -m "{Your commit message}"
   ```  

### 3. Resolve Merge Conflicts  
Always pull before pushing:  
```
git pull origin main  
git merge  
git push origin main  
```  

---  

## VIM Commands (for Git commit messages)  
```
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
