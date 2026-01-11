📁 GitHub Repository Structure
linux-user-group-management/
│
├── README.md
├── commands.sh
├── output.txt
└── screenshots/
    └── (optional – terminal screenshots)

📄 README.md (Copy–Paste Ready)
# 🐧 Beginner Linux Project – User & Group Management

This is a **beginner-level Linux administration project** focused on **User and Group Management**.  
The project demonstrates how system administrators manage users, groups, permissions, and sudo access in Linux.

---

## 📌 Project Objectives

- Create and delete users
- Create and manage groups
- Assign users to groups
- Grant sudo access
- Lock and unlock user accounts
- Understand Linux authentication files

---

## 🛠️ Commands Used

| Purpose | Command |
|------|--------|
| Create user | `useradd` |
| Delete user | `userdel` |
| Create group | `groupadd` |
| Modify user | `usermod` |
| Set password | `passwd` |
| Grant sudo | `usermod -aG sudo username` |
| Lock user | `passwd -l username` |
| Unlock user | `passwd -u username` |
| View groups | `groups username` |

---

## 🚀 Steps Performed

### 1️⃣ Create a User
```bash
sudo useradd user1
sudo passwd user1

2️⃣ Create a Group
sudo groupadd devteam

3️⃣ Add User to Group
sudo usermod -aG devteam user1

4️⃣ Give Sudo Access
sudo usermod -aG sudo user1

5️⃣ Lock & Unlock User
sudo passwd -l user1
sudo passwd -u user1

📂 Important System Files
File	Purpose
/etc/passwd	User account info
/etc/group	Group info
/etc/shadow	Encrypted passwords
📊 Output Verification
cat /etc/passwd | grep user1
cat /etc/group | grep devteam
groups user1

🎯 Learning Outcome

✔ Practical Linux user management
✔ Understanding sudo privileges
✔ Real-world system admin basics
✔ Interview-ready Linux project

🧑‍💻 Author

Kunal Bhatia
Beginner Linux & DevOps Learner 🚀

⭐ GitHub Tip

If you like this project, don’t forget to ⭐ star the repo!


---

## 📜 `commands.sh` (Optional but Professional)

```bash
#!/bin/bash

sudo useradd user1
sudo passwd user1

sudo groupadd devteam
sudo usermod -aG devteam user1

sudo usermod -aG sudo user1

sudo passwd -l user1
sudo passwd -u user1


Make it executable:

chmod +x commands.sh

📝 output.txt (Example)
user1:x:1001:1001::/home/user1:/bin/bash
devteam:x:1002:user1
user1 : user1 devteam sudo
