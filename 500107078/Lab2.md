Installing WSL (Windows Subsystem for Linux)
1. Enabling WSL
   To begin using WSL, it must first be enabled on your system.

Open PowerShell as an administrator.
Execute the following command:
sh
Copy
Edit
wsl --install
After installation, restart your computer to apply the changes.
2. Verifying WSL Installation
   To check the installed WSL version, use:

sh
Copy
Edit
wsl --list --verbose
If WSL 2 is not installed, update it with:

sh
Copy
Edit
wsl --update
3. Installing a Linux Distribution
   To view available Linux distributions, execute:

sh
Copy
Edit
wsl --list --online
Choose and install your preferred distribution (e.g., Ubuntu):

sh
Copy
Edit
wsl --install -d Ubuntu
Once installed, launch the distribution from the Start menu and follow the setup prompts to create a username and password.

4. Setting the Default WSL Version
   Ensure you are using WSL 2 by setting it as the default:

sh
Copy
Edit
wsl --set-default-version 2
To check and adjust the WSL version for a specific distribution:

sh
Copy
Edit
wsl --set-version Ubuntu 2
5. Updating the WSL Kernel
   If prompted that WSL 2 requires an update, install the latest WSL kernel from Microsoft's official site.

6. Running Linux Commands in WSL
   Linux commands can be used in:

The WSL terminal (Ubuntu or another installed distribution)
Windows Terminal
PowerShell or Command Prompt (by prefixing commands with wsl)
Example:

sh
Copy
Edit
wsl ls -la
7. Accessing Windows Files in WSL
   Windows files are accessible within WSL under /mnt/c/.

Navigate to your user directory with:

sh
Copy
Edit
cd /mnt/c/Users/YourUsername
ls
8. Uninstalling WSL
   To remove WSL from your system:

Uninstall any installed Linux distributions from Settings → Apps.
Run the following command in PowerShell (Admin) to unregister a distribution:
sh
Copy
Edit
wsl --unregister <DistroName>
Disable WSL features:
sh
Copy
Edit
dism.exe /online /disable-feature /featurename:Microsoft-Windows-Subsystem-Linux /norestart
Restart your system.