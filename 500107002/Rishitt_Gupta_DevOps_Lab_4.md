# Git Branching, Merging & Rebase

## Name: Rishitt Gupta  
**SAP ID:** 500107002  
**Enrollment Number:** R2142220352  
**Batch:** Full Stack AI B1 Hons  


## 1. **Setting Up a Project**
- **Create a project folder:**  
  ```sh
  mkdir project && cd project
  ```
- **Initialize Git:**  
  ```sh
  git init
  ```
- **Create some files:**  
  ```sh
  touch README.md s.txt
  ```

## 2. **Working with Files**
- Add text to `README.md`:  
  ```sh
  echo "Hello World" >> README.md
  ```
- View the file content:  
  ```sh
  cat README.md
  ```

## 3. **Basic Git Commands**
- **Check status:**  
  ```sh
  git status
  ```
- **Stage changes:**  
  ```sh
  git add .
  ```
- **Commit changes:**  
  ```sh
  git commit -m "Initial commit"
  ```

## 4. **Branching Basics**
- **Create and switch branches:**  
  ```sh
  git branch featureA
  git checkout featureA  # Switch to featureA
  ```
- **Shortcut for creating & switching:**  
  ```sh
  git checkout -b featureB
  ```

## 5. **Merging and Rebasing**
- **Merge `featureB` into `main`:**  
  ```sh
  git checkout main
  git merge featureB
  ```
- **Rebase `featureA` onto `main`:**  
  ```sh
  git checkout featureA
  git rebase main
  ```
- **Undo changes (hard reset):**  
  ```sh
  git reset --hard <commit-hash>
  ```

## 6. **Final Thoughts**
- Use **merge** when you want to keep branch history.  
- Use **rebase** for a cleaner, linear history.  
- Always **commit and push** your work frequently! 🚀  
