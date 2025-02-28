# DevOps Lab 5: Git Submodules  

## Details  
**Name:** Rishitt Gupta  
**SAP ID:** 500107002  
**Enrollment Number:** R2142220352  
**Batch:** Full Stack AI B1 Hons  

---  

## 1. Clone the Main Repository  
```
git clone "git@github.com:rishuu42/HTMLSide.git"
```  

## 2. Add Basic Files (HTML, CSS, JS)  

## 3. Add Submodules  
```
git submodule add "git@github.com:rishuu42/CSSSide.git"  
git submodule add "git@github.com:rishuu42/JSSide.git"  
```  

## 4. Push Submodules  
```
git add .  
git commit -m "Added Submodules"  
git push  
```  

## 5. Update CSS File & Commit  
```
git add .  
git commit -m "CSS updates"  
git push  
```  

## 6. Update Submodules  
```
git submodule update --remote --merge  
```  

## 7. Stage & Push Changes  
```
git add .  
git commit -m "CSS updates"  
git push  
```  

## 8. Update JS File & Commit  
```
git add .  
git commit -m "JS updates"  
git push  
```  

## 9. Update Submodules Again  
```
git submodule update --remote --merge  
```  

## 10. Final Commit  
```
git add .  
git commit -m "CSS updates"  
git push  
```  

## 11. Done
