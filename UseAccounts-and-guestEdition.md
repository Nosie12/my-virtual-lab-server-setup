# 🖥️ Part 3: User Accounts and Guest Edition in VirtualBox

In this lab, I focused on two main things:

1. Installing **Guest Edition** in VirtualBox to enable file sharing between the host and virtual machine.  
2. Creating **user accounts** in **Active Directory** on my Windows Server 2022 virtual machine.

---

## 🔧 Step 1: Install Guest Edition

To move files between my host machine and the virtual server, I installed **Guest Edition**:

1. Log into Windows Server 2022.
2. Insert Guest Edition CD from VirtualBox.
3. Follow the installer prompts: **Next → Next → Install**.
4. Reboot the VM when prompted.

### ⚡ Why this is important
- Guest Edition allows shared folders between the host and VM.
- Enables easy transfer of files for lab exercises.
- Makes practicing IT skills faster and more efficient without using the host machine directly.

---

## 📂 Step 2: Configure Shared Folder

1. In VirtualBox, go to **Shared Folders**.
2. Click **Add Folder** and select a folder on your host machine. I created one called `helpdesklab`.
3. Enable **Make Permanent** and **Automount**.
4. Log into the VM and verify that files can be copied into this folder.  

Example: I copied a JPEG logo into the folder to confirm it worked.

> ✅ This ensures I can move files into the VM for labs without complicated steps.

---

## 🏷️ Step 3: Create User Accounts in Active Directory

1. Open **Active Directory Users and Computers**.
2. Expand the domain and navigate to **Users**.
3. Right-click → **New → User**.
4. Enter the first user’s details:
   - Name: `Lisa`
   - Username: `lisa`
   - Password: Choose a secure password
5. Click **Next → Finish**.

### Additional Details
- You can fill in user profile information (address, job title, department, etc.) if required.
- Options include:
  - Reset password
  - Enable/disable account
  - Unlock account
  - Set logon hours

6. Repeat to create another user: `Kevin` (myself).

---

## 🔍 Step 4: Verify Accounts

- Command line:
```powershell
net user Mark /domain
