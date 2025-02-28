# DevOps Lab 2

## Name: Vyom Singhal
**SAP ID:** 500105031

**Roll Number:** R2142220212

**Batch:** Full Stack AI B1 Hons

## Installing WSL (Windows Subsystem for Linux)

WSL allows you to run Linux on Windows without a virtual machine. Below is a step-by-step guide to installing WSL on Windows.

---

## **Step 1: Enable WSL**

1. Open **PowerShell** as Administrator.
2. Run the following command to enable WSL:
   ```sh
   wsl --install
   ```
3. Restart your computer after installation.

---

## **Step 2: Check Installed WSL Version**  
Run the command to check which version of WSL is installed:  
```sh
wsl --list --verbose
```
If WSL 2 is not installed, update it using:  
```sh
wsl --update
```

---

## **Step 3: Install a Linux Distribution**  

1. Run the following command to see available Linux distributions:
   ```sh
   wsl --list --online
   ```
2. Install your preferred distribution (e.g., Ubuntu):
   ```sh
   wsl --install -d Ubuntu
   ```
3. Open **Ubuntu** (or the chosen distro) from the Start menu.
4. Set up a username and password when prompted.

---

## **Step 4: Set WSL Version**  
To ensure you're using WSL 2, set the default version:  
```sh
wsl --set-default-version 2
```
To check and change the version for a specific distro:  
```sh
wsl --set-version Ubuntu 2
```

---

## **Step 5: Update WSL Kernel (If Needed)**  

If you get an error about WSL 2 requiring an update, download and install the kernel update from Microsoft:  
[WSL Kernel Update](https://aka.ms/wsl2kernel)

---

## **Step 6: Running Linux Commands in WSL**

Once WSL is installed, you can use Linux commands directly from 
- The **WSL terminal** (`Ubuntu` or chosen distro)
- **Windows Terminal**
- **PowerShell** or **Command Prompt** (using `wsl` prefix)
  ```sh
  wsl ls -la
  ```

---

## **Step 7: Accessing Windows Files in WSL**
Your Windows files can be accessed from WSL under `/mnt/c/`.
```sh
cd /mnt/c/Users/YourUsername
ls
```
---

## **Additional Resources**
- [Official Microsoft WSL Documentation](https://docs.microsoft.com/en-us/windows/wsl/)