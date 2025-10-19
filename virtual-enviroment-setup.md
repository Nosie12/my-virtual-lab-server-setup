# Part 1: Setting Up the Virtual Environment 🛠️

Hi! In this part, I set up the foundation of my computer lab. I wanted a safe environment where I could practice IT skills without affecting my main system.


## Step 1: Install VirtualBox 💻

I downloaded **Oracle VirtualBox** because it allows me to run multiple operating systems on one computer. This is perfect for testing and learning IT skills safely.

- Go to [VirtualBox Download](https://www.virtualbox.org/wiki/Downloads)
- Download and install the latest version 


## Step 2: Download ISOs 🖥️

I needed two operating systems:

1. **Windows Server 2022** – this is the OS used in real-world networks to manage users, computers, and resources.
   - Go to [Microsoft Server ISO](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022)
   - Download the 64-bit edition

2. **Windows 11** – I plan to join this to the server later.
   - Go to [Windows 11 Media Creation](https://www.microsoft.com/software-download/windows11)
   - Download the ISO


## Step 3: Create a Virtual Machine 🖱️

I created a VM in VirtualBox for Windows Server 2022:

- Click **New** → Name: `Server2022`
- Type: `Microsoft Windows` → Version: `Windows 2022 (64-bit)`
- Assign **CPU and memory**: I used 2 CPUs and 8GB RAM
- Attach the ISO under **Storage**
- Select **Desktop Experience** during installation so I could interact with it like a normal computer


## Step 4: Install Windows Server 2022 ⚡

- Start the VM
- Follow the installation steps
- Choose **Custom installation**
- Complete installation and set a password
- Adjust **time zone** to match your location
- After installation, I practiced shutting down using both:
  - **GUI:** Start → Power → Shut Down
  - **Command Line:**  
    ```cmd
    shutdown /s /t 0 # Shut down immediately
    shutdown /r /t 0 # Restart immediately
    ```

## Why This Step Is Important ✅

Creating a virtual environment allows me to experiment safely. I can install, configure, and break things without affecting my main computer. It’s the foundation for all IT lab exercises.


**Skills Gained:**

- Virtual machine creation
- Windows Server 2022 installation
- Safe testing environment
- Basic shutdown/restart commands
