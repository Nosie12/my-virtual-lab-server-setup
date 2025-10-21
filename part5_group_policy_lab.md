# Part 5 – Group Policy and Account Management (Active Directory Lab)

## 🎯 Objective
In this part of the lab, I practiced managing user accounts and implementing **Group Policy** on the Domain Controller. This simulates how IT professionals handle account restrictions, password policies, and lockout policies in a corporate environment.

---

## 🖥️ Lab Setup
- **Server:** Windows Server 2022 acting as Domain Controller
- **Client Machine:** Windows 11 joined to the domain
- **Users:** Example user "Mark" (simulated employee)

---

## 🔧 Managing User Accounts

### 1. Disabling a User Account
- Open **Active Directory Users and Computers**
- Locate the user (e.g., Mark)
- Right-click → **Disable Account**
- Reboot client machine to test
- Sign in with a local admin account if necessary
- Delete cached profiles to fully replicate disable behavior

### 2. Testing Account Restrictions
- Attempt to log in as the disabled user → login fails
- Re-enable account to restore access
- Experiment with:
  - **Login hours** (restrict when users can log in)
  - **Account expiration** (set a date or “never”)
  - Observe error messages like:
    - "Account has time restrictions"
    - "User account has expired"

---

## 🔧 Group Policy Configuration

### 1. Open Group Policy Management
- Go to **Server Manager → Tools → Group Policy Management**
- Navigate to your domain → **Default Domain Policy**
- Right-click → **Edit**

### 2. Configure Policies
- **Password Policy:**
  - Maximum password age: 90 days
  - Minimum password age: 1 day
  - Recommended password length: 12+ characters
- **Account Lockout Policy:**
  - Lockout threshold: 3 invalid attempts
  - Lockout duration: 360 minutes (can vary by organization)
  - Reset counter after: 30 minutes
- **Explanation:** These settings help prevent unauthorized access or brute-force attacks.

### 3. Apply Policies
- Right-click the GPO → **Enforce**
- Verify with commands:
  - `net user Mark /domain` → shows password last set, expiration, groups
  - `gpresult /R` → shows applied policies on the client

---

## 🔐 Real-World Practice
- Reset passwords for users
- Lock and unlock accounts
- Enforce login restrictions
- Observe error messages as in real IT support scenarios
- Helps simulate help desk or MSP (Managed Service Provider) tasks

---

## 🧠 Skills Demonstrated in Part 5

| Skill | Description |
|-------|-------------|
| User Account Management | Disable, enable, reset, and delete accounts |
| Group Policy Management | Set password, lockout, and login restrictions |
| Active Directory Practice | Navigate ADUC, enforce policies, verify domain settings |
| Troubleshooting | Handle login failures, cached profiles, and errors |
| IT Support Simulation | Mimic real-world help desk scenarios |

---

## ✅ Summary
By the end of Part 5, I had:
- Disabled and re-enabled user accounts
- Configured password and lockout policies in Group Policy
- Practiced troubleshooting login issues
- Gained a better understanding of how corporate IT environments enforce security standards

---

## 🚀 Next Steps (Part 6 Preview)
In the next part, I will:
- Start installing software on client machines using Group Policy
- Explore shared folders and permissions
- Continue building a complete simulated enterprise environment
