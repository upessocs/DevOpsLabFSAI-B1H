# DevOps Lab 1  
# CI/CD Basics  

Continuous Integration (CI) and Continuous Deployment (CD) streamline software development by automating testing and deployment.

## Name: Rishitt Gupta  
**SAP ID:** 500107002  
**Enrollment Number:** R2142220352  
**Batch:** Full Stack AI B1 Hons  

---

## **1. What is CI/CD?**  
- **Continuous Integration (CI):** Developers merge code frequently, and automated tests run to detect issues early.  
- **Continuous Deployment (CD):** Code changes are automatically deployed to production after passing all tests.

## **2. Install Git & CI/CD Tools**  
Install Git and CI/CD tools like Jenkins or GitHub Actions.  
```sh
sudo apt update && sudo apt install git -y
```

## **3. Set Up a Git Repository**  
1. Initialize Git:  
   ```sh
   git init
   ```
2. Add remote repository:  
   ```sh
   git remote add origin <repo-url>
   ```
3. Commit and push changes:  
   ```sh
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

## **4. Benefits of CI/CD**  
- **Faster Deployment**: Automates the software release process.  
- **Early Bug Detection**: Catches errors before deployment.  
- **Efficiency**: Reduces manual intervention.  