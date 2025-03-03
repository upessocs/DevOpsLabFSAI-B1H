## Setting up WSL (Lab 2) :

Step 1: Enable WSL
Open PowerShell as Administrator:

Right-click on the Start button and select Windows Terminal (Admin) or PowerShell (Admin).
Install WSL:

Run the following command to enable WSL and install the default Linux distribution (typically Ubuntu):
```
wsl --install
```
Restart Your Computer:

A system reboot may be required to complete the installation process.
Step 2: Verify the WSL Installation
To verify which version of WSL is installed, execute the following command:
```
wsl --list --verbose
```
If WSL 2 is not installed, update it using:
```
wsl --update
```
Step 3: Install a Linux Distribution
List Available Distributions:
```
wsl --list --online
```
Install Your Preferred Distribution: For example, to install Ubuntu, execute:
```
wsl --install -d Ubuntu
```
Set Up the Linux Environment: Launch Ubuntu (or your chosen distribution) from the Start menu and follow the setup prompts to create a username and password.

Step 4: Configure WSL Version to WSL 2
Set WSL 2 as the default version by running:
```
wsl --set-default-version 2
```
To apply WSL 2 to a specific distribution:
```
wsl --set-version Ubuntu 2
```
Step 5: Update the WSL Kernel (Optional)
If prompted to update WSL 2, download and install the latest kernel update from Microsoft: Download WSL Kernel Update

Step 6: Execute Linux Commands in WSL
You can now run Linux commands through:

The WSL terminal (e.g., Ubuntu or other distributions)
Windows Terminal
PowerShell or Command Prompt, using the wsl prefix:
```
wsl ls -la
```
Step 7: Access Windows Files from WSL
Access your Windows files from the WSL terminal using the /mnt/c/ directory:
```
cd /mnt/c/Users/YourUsername
ls
```

