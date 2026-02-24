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

**Screenshot:** Administrator Command Prompt window 

<img width="435" height="145" alt="Step 1 Command prompt" src="https://github.com/user-attachments/assets/cef2aee5-c9e2-4fd8-a386-283553a959d3" />

---

# Step 2: Create a New User

### Command Breakdown:
- `net user` → Manages user accounts
- `student1` → Username created
- `Password123` → Assigned password
- `/add` → Creates the account

This confirms the new local user account was created.

**Screenshot:** New User Created

<img width="500" height="184" alt="Step 2 create a new user" src="https://github.com/user-attachments/assets/5fdb1899-9b04-4178-9aff-4f11e0786068" />

The username `student1` appears in the list of accounts.

### Result: The command completed successfully.

---

# Step 3: Add User to Administrators Group

### Command Used: net localgroup Administrators student1 /add

### Command Breakdown:
- `net localgroup` → Manages local groups
- `Administrators` → Group with full system privileges
- `student1` → User being added
- `/add` → Adds user to group

This confirms `student1` now has administrative privileges.

**Screenshot:** Group addition confirmation 

<img width="570" height="193" alt="Step 3 Add user to Administrators Group" src="https://github.com/user-attachments/assets/663ef428-82a7-447c-80e5-60cc9f0a13d9" />

`student1` appears in the Administrators group list.

### Result:The command completed successfully.

---

# Step 4: Create a Folder

### Command Used:mkdir C:\ProjectFolder

New folder named `ProjectFolder` in the C:\ directory have been created.

### Verification:dir C:\

The folder `ProjectFolder` appears in the directory listing.

**Screenshot:** Folder creation confirmation

<img width="457" height="180" alt="Step 4 create the folder" src="https://github.com/user-attachments/assets/22f2ac77-2162-40d2-bb3d-351931ae48b4" />

---

# Step 5: Modify Folder Permissions

### Command Used:icacls C:\ProjectFolder /grant student1:F

### Command Breakdown:
- `icacls` → Tool for managing file and folder permissions
- `C:\ProjectFolder` → Target folder
- `/grant` → Grants specified permissions
- `student1` → User receiving permissions
- `F` → Full control access

This confirms that `student1` has full control over the folder.

### Verification (Optional):icacls C:\ProjectFolder

**Screenshot:** Permission modification confirmation

<img width="534" height="184" alt="Step 5 Grant Full Control Permission" src="https://github.com/user-attachments/assets/9b61167c-63aa-4bb0-920f-f58861381c71" />

### Result:Successfully processed 1 files

---

# Step 6: Install Git Using Chocolatey

## Step 6.1: Confirm Chocolatey Installation

A version number confirms Chocolatey is installed.

**Screenshot:** Chocolatey version output

<img width="273" height="85" alt="step 6 1 Choco Installation" src="https://github.com/user-attachments/assets/3f0bd25b-f7a0-4152-9a32-edb7c7d9ec27" />


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

