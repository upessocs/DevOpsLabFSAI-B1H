# DevOps Lab 4: Git Branching, Merging & Rebase  

## Details  
**Name:** Rishitt Gupta  
**SAP ID:** 500107002  
**Enrollment Number:** R2142220352  
**Batch:** Full Stack AI B1 Hons  

---  

## 1. Setting Up a Project  
```
mkdir project && cd project  
git init  
touch README.md s.txt  
```  

## 2. Working with Files  
```
echo "Hello World" >> README.md  
cat README.md  
```  

## 3. Basic Git Commands  
```
git status  
git add .  
git commit -m "Initial commit"  
```  

## 4. Branching Basics  
Create and switch branches:  
```
git branch featureA  
git checkout featureA  
```  

## 5. Merging and Rebasing  
Merge `featureB` into `main`:  
```
git checkout main  
git merge featureB  
```  
Rebase `featureA` onto `main`:  
```
git checkout featureA  
git rebase main  
```  
Undo changes (hard reset):  
```
git reset --hard <commit-hash>  
```