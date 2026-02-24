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

**Command Prompt:**
The Command Prompt provides direct interaction with the operating system for executing system-level commands. Running it as **Administrator** grants elevated permissions required for creating users, modifying groups, changing folder permissions, and installing software.  

**Screenshot:** Administrator Command Prompt window 

<img width="435" height="145" alt="Step 1 Command prompt" src="https://github.com/user-attachments/assets/cef2aee5-c9e2-4fd8-a386-283553a959d3" />

---

# Step 2: Create a New User

**Description:**  
This creates a new local user (`student1`) by adding an entry to Windows’ Security Accounts Manager (SAM), assigning a unique SID, hashing the password securely, and giving default Users group membership.  

This confirms the new local user account was created.

**Screenshot:** New User Created

<img width="500" height="184" alt="Step 2 create a new user" src="https://github.com/user-attachments/assets/5fdb1899-9b04-4178-9aff-4f11e0786068" />

The username `student1` appears in the list of accounts.

### Result: The command completed successfully.

---

# Step 3: Add User to Administrators Group

### Command Used: net localgroup Administrators student1 /add

**Description:**  
Adds `student1` to the Administrators group, granting full system privileges. This demonstrates understanding of group management, privilege escalation, and access control.  

This confirms `student1` now has administrative privileges.

**Screenshot:** Group addition confirmation 

<img width="570" height="193" alt="Step 3 Add user to Administrators Group" src="https://github.com/user-attachments/assets/663ef428-82a7-447c-80e5-60cc9f0a13d9" />

`student1` appears in the Administrators group list.

### Result:The command completed successfully.

---

# Step 4: Create a Folder

### Command Used:mkdir C:\ProjectFolder

**Description:**  
Creates a folder `ProjectFolder` in C:\ using the CLI, demonstrating file system management via command line.  

New folder named `ProjectFolder` in the C:\ directory have been created.

### Verification:dir C:\

The folder `ProjectFolder` appears in the directory listing.

**Screenshot:** Folder creation confirmation

<img width="457" height="180" alt="Step 4 create the folder" src="https://github.com/user-attachments/assets/22f2ac77-2162-40d2-bb3d-351931ae48b4" />

---

# Step 5: Modify Folder Permissions

### Command Used:icacls C:\ProjectFolder /grant student1:F

**Description:**  
Grants `student1` **full control** over the folder, updating Access Control Lists (ACLs) to manage permissions securely. Demonstrates understanding of file system security and user access management.  

This confirms that `student1` has full control over the folder.

### Verification (Optional):icacls C:\ProjectFolder

**Screenshot:** Permission modification confirmation

<img width="534" height="184" alt="Step 5 Grant Full Control Permission" src="https://github.com/user-attachments/assets/9b61167c-63aa-4bb0-920f-f58861381c71" />

### Result:Successfully processed 1 files

---

# Step 6: Install Git Using Chocolatey

## Step 6.1: Chocolately Installation

A version number confirmed that:

- Chocolatey was correctly installed.
- The system PATH environment variable was properly configured.
- The CLI could locate and execute the `choco` command.

Package managers such as Chocolatey improve system administration efficiency by eliminating manual downloads, reducing configuration errors, and enabling automated deployments.

**Screenshot:** Chocolatey version output

<img width="273" height="85" alt="step 6 1 Choco Installation" src="https://github.com/user-attachments/assets/3f0bd25b-f7a0-4152-9a32-edb7c7d9ec27" />

---

## Step 6.2: Git Installation Process

# Git Installation Process Using Chocolatey

### Technical Breakdown:

- `choco` invokes the Chocolatey package manager.
- `install` instructs Chocolatey to retrieve and install a specified package.
- `git` identifies the target package from the repository.
- `-y` automatically accepts all prompts, enabling non-interactive installation.

During execution, Chocolatey performed the following operations:

1. Queried the Chocolatey online repository.
2. Downloaded the latest stable Git package.
3. Executed installation scripts.
4. Configured required system settings.
5. Updated environment variables if necessary.

This method ensures a controlled and repeatable deployment process, which is essential in professional IT environments.

### Command Breakdown:
- `choco` → Chocolatey package manager
- `install` → Install a package
- `git` → Package name
- `-y` → Automatically accept installation prompts

The system downloads and installs Git.

**Screenshot:** Git installation process

<img width="650" height="311" alt="Step6 1 Installing Git" src="https://github.com/user-attachments/assets/25302624-68c6-44e7-897c-4abff77d6913" />

---

## Step 6.3: Verication of Git Installation

## Verification of Git Installation

After installation, Git was verified using: git --version

This command serves multiple technical purposes:

- Confirms that Git was successfully installed.
- Verifies that the executable is accessible via the system PATH.
- Ensures the CLI can properly invoke the Git binary.

If the installation was successful, the system displayed the installed Git version (e.g., `git version 2.xx.x.windows.x`).

This verification step confirms operational readiness and validates that the package manager correctly configured the environment.

---

## Technical Significance

The use of Chocolatey demonstrates understanding of:

- Software package management
- Automated installation processes
- Environment variable configuration
- Command-line system administration
- Verification and validation of deployed software

In enterprise environments, package managers are essential for maintaining consistency, improving efficiency, and reducing human error during software deployment.

The installed Git version is displayed, confirming successful installation.

**Screenshot:** Git version confirmation

<img width="701" height="341" alt="Step 6 2 Installing Git" src="https://github.com/user-attachments/assets/4ea57bb4-c427-4729-84c6-d044bf94b15a" />

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

