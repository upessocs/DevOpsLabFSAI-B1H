# DevOps Lab 2
# Installing WSL (Windows Subsystem for Linux)

WSL allows you to run Linux on Windows without a virtual machine.

## **1. Install WSL**
Run in **PowerShell (Admin)**:  
```sh
wsl --install
```
Restart your PC.

## **2. Install a Linux Distro**  
Check available distros:  
```sh
wsl --list --online
```
Install one (e.g., Ubuntu):  
```sh
wsl --install -d Ubuntu
```
Open it from the **Start menu** and set up a user.

## **3. Use WSL**  
Run Linux commands:  
```sh
wsl ls -la
```
Access Windows files:  
```sh
cd /mnt/c/
```

## **4. Uninstall WSL**  
1. Remove distros from **Settings > Apps**.  
2. Run in **PowerShell (Admin)**:  
   ```sh
   wsl --unregister <DistroName>
   dism.exe /online /disable-feature /featurename:Microsoft-Windows-Subsystem-Linux
   ```
3. Restart your PC.