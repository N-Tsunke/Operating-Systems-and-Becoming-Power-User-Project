# Operating-Systems-and-Becoming-Power-User-Project

## Practical Task: User & File Management (Windows)

---

## Objective

This practical exercise demonstrates practical knowledge of:

- Windows user account management  
- Group membership management  
- File system and permission control  
- Command-line package management using Chocolatey  

All tasks were performed using the Windows Command Prompt with administrative privileges.

---

## Environment

- Operating System: Windows  
- Interface: Command Prompt (Run as Administrator)  
- Package Manager: Chocolatey  
- Software Installed: Git  

---

# Step 1: Open Command Prompt as Administrator

**Screenshot:** Administrator Command Prompt window <img width="970" height="236" alt="Step 1 Command prompt" src="https://github.com/user-attachments/assets/fc3a1061-e01f-4907-bdd4-444952bf9bfb" />

---

# Step 2: Create a New User

### Command Breakdown:
- `net user` → Manages user accounts
- `student1` → Username created
- `Password123` → Assigned password
- `/add` → Creates the account

### Result: The command completed successfully.

This confirms the new local user account was created.

**Screenshot:** Successful user creation <img width="500" height="184" alt="Step 2 create a new user" src="https://github.com/user-attachments/assets/5fdb1899-9b04-4178-9aff-4f11e0786068" />


# Verification (Optional): net user

The username `student1` appears in the list of accounts.

---

# Step 3: Add User to Administrators Group

### Command Used: net localgroup Administrators student1 /add

### Command Breakdown:
- `net localgroup` → Manages local groups
- `Administrators` → Group with full system privileges
- `student1` → User being added
- `/add` → Adds user to group

### Result:The command completed successfully.


This confirms `student1` now has administrative privileges.

## Screenshot: Group addition confirmation

### Verification (Optional): net localgroup Administrators

`student1` appears in the Administrators group list.

---

# Step 4: Create a Folder

### Command Used:mkdir C:\ProjectFolder

This creates a new folder named `ProjectFolder` in the C:\ directory.

### Verification:dir C:\

The folder `ProjectFolder` appears in the directory listing.

## Screenshot: Folder creation confirmation

---

# Step 5: Modify Folder Permissions

### Command Used:icacls C:\ProjectFolder /grant student1:F

### Command Breakdown:
- `icacls` → Tool for managing file and folder permissions
- `C:\ProjectFolder` → Target folder
- `/grant` → Grants specified permissions
- `student1` → User receiving permissions
- `F` → Full control access

### Result:Successfully processed 1 files

This confirms that `student1` has full control over the folder.

## Screenshot: Permission modification confirmation

### Verification (Optional):icacls C:\ProjectFolder

---

# Step 6: Install Git Using Chocolatey

## Step 6.1: Confirm Chocolatey Installation

A version number confirms Chocolatey is installed.

## Screenshot: Chocolatey version output

---

## Step 6.2: Install Git

choco install git -y

### Command Breakdown:
- `choco` → Chocolatey package manager
- `install` → Install a package
- `git` → Package name
- `-y` → Automatically accept installation prompts

The system downloads and installs Git.

## Screenshot: Git installation process

---

## Step 6.3: Verify Installation

git --version


The installed Git version is displayed, confirming successful installation.

## Screenshot: Git version confirmation

---

# Overall Summary

In this practical task, I successfully:

- Created a new user account (`student1`)
- Assigned administrative privileges to the user
- Created a directory using command-line tools
- Modified file system permissions using `icacls`
- Installed Git using the Chocolatey package manager
- Verified all configurations using appropriate CLI commands

This exercise demonstrates practical understanding of:

- Windows user and group management
- File system permission structures
- Command-line system administration
- Software installation using a package manager

---

# Screenshots Included

- Administrator Command Prompt
- User account creation
- Administrator group assignment
- Folder creation
- Permission modification
- Chocolatey version check
- Git installation process
- Git version verification

---

#  Learning Outcome

Through this exercise, I developed hands-on experience in Windows system administration tasks using the command line, strengthening my understanding of operating systems, access control, and package management.

