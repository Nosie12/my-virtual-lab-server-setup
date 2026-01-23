# Active Directory Home Lab (Windows Server 2022 & Windows 11)

This repository documents my hands-on Active Directory home lab.  
The goal of this lab is to understand how enterprise Windows environments work, including domain setup, user management, and Group Policy.

Each markdown file represents a different stage of the lab, written step by step to show what I configured and what I learned.

---

## 🧪 Lab Environment

- **Server OS:** Windows Server 2022  
- **Client OS:** Windows 11  
- **Virtualization:** VirtualBox  
- **Directory Service:** Active Directory Domain Services (AD DS)  
- **Domain:** Custom internal domain  
- **Networking:** Host-only / internal network

---

## 📂 Repository Files

### 1. `virtual-enviroment-setup.md`
This file covers:
- Creating the virtual machines
- Configuring VirtualBox networking
- Setting up the basic lab environment
- Preparing the server and client machines

This is the foundation of the entire lab.

---

### 2. `turn-server-to-domain-controller.md`
This file explains:
- Installing Active Directory Domain Services
- Promoting Windows Server 2022 to a Domain Controller
- Configuring DNS
- Creating the domain

This is where the server becomes the central controller of the network.

---

### 3. `UseAccounts-and-guestEdition.md`
This section focuses on:
- Creating domain user accounts
- Understanding guest vs standard users
- Managing users through Active Directory
- Practicing basic identity management

This simulates how real companies manage employee accounts.

---

### 4. `windows11_domain_join.md`
This file documents:
- Configuring Windows 11 networking
- Joining the Windows 11 machine to the domain
- Verifying domain connectivity
- Confirming the client appears in Active Directory

This represents adding a workstation to a corporate network.

---

### 5. `part5_group_policy_lab.md`
This part focuses on:
- Group Policy Management
- Password policies
- Account lockout policies
- Disabling and enabling user accounts
- Simulating real help desk scenarios
- Troubleshooting login issues

This is where centralized control and security management begins.

---

## 🎯 What I Practiced

- Active Directory administration  
- Domain controller configuration  
- DNS fundamentals  
- Windows client domain joining  
- Group Policy security settings  
- User account troubleshooting  
- Help desk style IT scenarios  

---

## 🚀 Why I Built This Lab

I built this lab to:
- Gain real-world IT experience
- Understand how corporate environments work
- Practice help desk and system administration tasks
- Strengthen my networking and Windows server skills

This lab mirrors what IT professionals do daily in enterprise environments.

---

## 🔧 Future Improvements

- Software deployment via Group Policy  
- Shared folders and permissions  
- Login scripts  
- OU structure design  
- Security hardening  
- Windows updates management  

---

## 📌 Note

This lab is for learning and practice purposes only and was built in a local virtual environment.

---

**Author:** Nosipho Sithole  
**Focus:** IT Support | Active Directory | Networking | System Administration
