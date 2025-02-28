# LAB-2

To install **Windows Subsystem for Linux (WSL)** on your Windows machine, follow these steps:

1. Name- Divya Darshan Tiwari
2. SAP- 500105299
3. Roll No. - R2142220070
4. Batch - B1H Full Stack AI

### **1. Enable WSL**

Open **PowerShell as Administrator** and run:

```powershell
wsl --install

```

This will:

- Enable the WSL feature
- Install the latest version of WSL 2
- Install Ubuntu (default distribution)
- now will ask to install ubuntu say yes
- will ask password , set it and done

**Restart your computer** if prompted.

---

### **3. Set WSL Version (WSL 2)**

Check the installed version:

```powershell
wsl --list --verbose

```

### **5. Update WSL (If Needed)**

Ensure WSL is up to date:

```powershell
wsl --update

```

---

### **6. Launch WSL**

Open WSL by typing:

```powershell
wsl

```

Or open your installed distribution from the **Start Menu**.

---

Click window button in the and search ubnatu

### **5. Install Docker on WSL**

To install **Docker** on WSL, follow these steps:

#### **Step 1: Install Docker Desktop**

1. Download **Docker Desktop for Windows** from the official Docker website:  
   [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)
2. Run the installer and follow the setup instructions.
3. Ensure you **enable WSL 2** during installation.
4. Restart your computer if required.

#### **Step 2: Enable Docker Support for WSL**

1. Open **Docker Desktop**.
2. Navigate to **Settings > General**.
3. Enable **Use the WSL 2 based engine**.
4. Apply the settings and restart Docker.

#### **Step 3: Verify Docker Installation**

After installation, verify that Docker is working inside WSL:

```bash
docker --version
docker run hello-world
```

If you see a message saying **Hello from Docker!**, then Docker is installed successfully.

---

Click the **Windows button**, search for **Ubuntu**, and launch it to start using WSL.
