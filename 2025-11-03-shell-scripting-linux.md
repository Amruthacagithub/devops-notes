# Class Notes – Shell Scripting & Linux (Today)

### Variables & User Input

* Variable syntax: `NAME=value`
* Access variable using: `$NAME`
* Take user input with: `read -p`

Example:

```bash
read name
echo $name
```

---

### Conditions & Loops

* `if [ condition ]` → Used for decision making
* `-f file` → Checks whether a file exists
* `for` and `while` → Used for looping/repetition

Commonly used for automation tasks.

---

### Scripts Practiced in Class

* Display current date and time
* Monitor disk usage
* Verify if a file exists
* Perform arithmetic operations
* Check internet connectivity
* Backup directories
* Verify logged-in users
* Display system uptime

Scripts help simplify and automate admin tasks.

---

### Docker / Bash Script Execution

* Bash-only features do not work with `sh`
* Always run Bash scripts using `./script.sh`
* Running with `sh script.sh` may cause errors

---

### Bash vs Sh Comparison

| Feature         | Bash      | Sh            |
| --------------- | --------- | ------------- |
| Arrays          | Supported | Not supported |
| String handling | Supported | Limited       |
| Speed           | Moderate  | Faster        |
| Features        | Advanced  | Basic         |

* Prefer **bash** for complex scripts.

---

### String Operations

* `${str}` → Access variable value
* `${str^^}` → Convert to uppercase
* `${str,,}` → Convert to lowercase
* `rev` → Reverse a string
* Substring → `${str:position:length}`

---

### Functions & Code Reuse

* Functions help reuse common logic
* Scripts can include other scripts

Example:

```bash
source utils.sh
```

Used widely in automation and projects.

---

### User & Group Management Script

* Uses `useradd` and `groupadd`
* Script validates:

  * Root permissions
  * Input arguments
  * Existing users/groups
* Error handling makes scripts professional.

---

### Automation Assignment Learnings

* Created reusable utility functions
* Added timestamps to folder names
* Used `date` command
* Followed modular scripting practices
* Improved automation skills

---

### File Permissions

* `rwx` → Read, Write, Execute
* `chmod` → Modify permissions
* `chown` → Change ownership
* `chgrp` → Change group

Example:

```bash
chmod 755 file.sh
```

---

## 🔐 Access Control Lists (ACL)

### What is ACL?

* Provides different permissions to multiple users
* More flexible than standard chmod

---

### Important ACL Commands

* View ACL → `getfacl file`
* Set ACL → `setfacl`
* Remove entry → `setfacl -x`
* Remove all ACLs → `setfacl -b`

Example:

```bash
setfacl -m u:john:rw file.txt
```

---

### Default ACL

* Automatically applies permissions to new files
* Commonly used in shared directories

---

### Mask in ACL

* Restricts maximum effective permissions
* Can limit access even if higher permissions are assigned

---

### ACL Usage in Scripts

* Useful for shared team folders
* Automatically assigns access permissions

---

## Key Takeaways

* Shebang defines the shell interpreter
* Bash offers more features than sh
* Always assign execute permission to scripts
* Use functions for reusable code
* Error handling is essential
* ACL enables advanced permission control
* Automation improves efficiency
* Be extremely careful with `rm -rf`
