# DevOps Lab 2: Installing WSL  

WSL lets you run Linux on Windows without a virtual machine.  

## Details  
**Name:** Rishitt Gupta  
**SAP ID:** 500107002  
**Enrollment Number:** R2142220352  
**Batch:** Full Stack AI B1 Hons  

---  

## 1. Install WSL  
Run in **PowerShell (Admin)**:  
```
wsl --install
```  
Restart your PC.  

## 2. Install a Linux Distro  
Check available distros:  
```
wsl --list --online
```  
Install one (e.g., Ubuntu):  
```
wsl --install -d Ubuntu
```  
Open it from the **Start menu** and set up a user.  

## 3. Use WSL  
Run Linux commands:  
```
wsl ls -la
```  
Access Windows files:  
```
cd /mnt/c/
```  

## 4. Uninstall WSL  
1. Remove distros from **Settings > Apps**.  
2. Run in **PowerShell (Admin)**:  
   ```
   wsl --unregister <DistroName>
   dism.exe /online /disable-feature /featurename:Microsoft-Windows-Subsystem-Linux
   ```
3. Restart your PC.  

Link For Lab 3 - [Lab 3](./Rishitt_Gupta_DevOps_Lab_3.md)