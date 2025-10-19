# Part 2: Turning the Server into a Domain Controller 🏛️


Hi again! In this part, I took the virtual server from Part 1 and turned it into a **Domain Controller** using **Active Directory Domain Services (AD DS)**.


## Step 1: Rename the Server 🏷️

I renamed my server to something meaningful so it’s easy to identify in a network:

- Open **Local Server**
- Click **Computer Name → Change**
- Rename: `my-dc01` (DC = Domain Controller)
- Restart the server


## Step 2: Install Active Directory Domain Services 🛠️

- Open **Server Manager → Manage → Add Roles and Features**
- Select **Active Directory Domain Services**
- Click **Next → Install**
- Wait for installation to complete


## Step 3: Promote the Server to a Domain Controller ⚡

- Click the **notifications flag** → Promote this server
- Choose **Add a new forest**
- Domain Name: `nosipho.com` (you can pick any name)
- Set a **Directory Services Restore Mode (DSRM) password**
- Click **Next → Install**
- Server will restart automatically


## Step 4: Using PowerShell (Optional) 🖥️

I also tried installing AD DS via PowerShell for a more professional approach:

```powershell
Install-ADDSForest `
-DatabasePath "C:\Windows\NTDS" `
-DomainMode "Win2016" `
-DomainName "nosipho.com" `
-InstallDNS:$true `
-LogPath "C:\Windows\NTDS" `
-SysvolPath "C:\Windows\SYSVOL" `
-Force
```


## Step 5: Verify the Domain Controller ✅

After setting up my Domain Controller, I verified that everything was working correctly using both the **command line** and **Active Directory tools**.


## Using Command Line 🖥️

```cmd
whoami # Shows the logged-in user and domain `
net accounts # Checks account policies `
systeminfo # Displays detailed server information `
```

## Using Active Directory Tools 🛠️

- Open **Active Directory Users and Computers**  
- Check the **domain structure** and verify the **administrator account**


## Why This Step Is Important ✅

A Domain Controller is central to network management. It manages users, computers, and security policies. By verifying the setup, I can:

- Centrally control users and computers  
- Enforce security policies  
- Add other computers (like Windows 11) to the domain  
- Practice real-world IT networking skills  


## Skills Gained ⭐

- Active Directory setup and management  
- Domain Controller configuration  
- PowerShell basics  
- Windows 11 domain joining  
- Network administration fundamentals
