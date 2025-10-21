# Part 4 – Windows 11 Domain Join (Active Directory Lab)

## 🎯 Objective
In this part of the lab, I installed and configured a Windows 11 virtual machine, configured its network settings, and successfully joined it to my Active Directory domain. This simulates how IT professionals add client machines to a corporate network environment for centralized management.

---

## 🖥️ Virtual Machine Setup (Windows 11)

### ✅ Steps:
1. **Create a New Virtual Machine in VirtualBox**
   - OS: Windows 11 Pro or Enterprise (Home editions do not support domain joining)
   - RAM: Minimum 4GB
   - Network Adapter: Set to **Host-Only Adapter** or **Bridged Adapter** (must match the Domain Controller's network)

2. **Configure Network Settings**
   - Disable internet temporarily to bypass Microsoft account requirements
   - Manually assign an IP address in the same subnet as the Domain Controller

   **Example:**

---

## 🌐 Domain & Network Summary

| Component       | IP Address   | Role                  |
|----------------|--------------|-----------------------|
| Server 2022    | 10.1.10.1    | Domain Controller + DNS |
| Windows 11 VM  | 10.1.10.3    | Domain Client         |
| Domain Name    | keftte.com   | Active Directory Domain |

---

## 🔧 Joining the PC to the Domain

### 📌 Steps to Join
1. Right-click **This PC** → **Properties**
2. Click **Rename this PC (Advanced)**
3. Select **Domain**, enter:
4. Enter domain administrator credentials:
5. A success message appears:  
**"Welcome to the keftte.com domain"**
6. Restart the machine.

---

## 🧪 Verification Commands (After Restart)
Open **Command Prompt** on the Windows 11 machine and run:

These commands confirm that the machine is connected and authenticated to the domain.

---

## 🔍 Active Directory Confirmation
On the Domain Controller:

1. Open **Active Directory Users and Computers**
2. Navigate to:
3. You should now see the Windows 11 machine listed.

---

## 🔐 Optional: Enable Remote Desktop
To allow remote management:

1. Right-click **This PC**
2. Select **Remote Desktop Settings**
3. Enable **Allow remote connections**
4. Add domain users (like Administrator or custom users)

---

## 🎯 Why This Step Is Critical
Joining a client machine to a domain allows centralized management:
- Group Policy deployment
- User authentication from one place
- Security and access control
- Real-world IT enterprise simulation

This is exactly what happens in professional IT environments.

---

## 🧠 Skills Demonstrated in Part 4

| Skill | Description |
|------|-------------|
| Active Directory Integration | Joining devices to a domain |
| DNS Configuration | Ensures domain communication |
| VM Networking | Host-only and bridged networking concepts |
| Windows Administration | Installation, configuration, domain join |
| Remote Management | Using RDP and domain credentials |

---

## ✅ Summary
By the end of Part 4, I had:
- A Windows Server 2022 acting as the Domain Controller
- A Windows 11 client successfully joined to the domain
- Verified connectivity and trust between both machines
- Prepared the environment for Group Policy, shared folders, and future enterprise features like Intune

---

## 🚀 Next Steps (Part 5 Preview)
In the next part, I will:
- Configure **Group Policy Management**
- Apply policies to users and computers
- Create and manage **Organizational Units (OUs)**
- Implement login scripts and folder redirection

> This is where true centralized control begins 🚀

---
