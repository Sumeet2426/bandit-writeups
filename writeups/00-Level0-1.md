# Bandit Level 0 → 1

## Objective

Connect to the Bandit server using SSH and retrieve the password for Bandit Level 1.

---

## Challenge Description

The goal of this level is to establish a secure SSH connection to the Bandit server and locate the password stored in a file.

---

## Enumeration

After connecting to the remote machine, I listed the contents of the current directory to identify any files containing useful information.

---

## Commands Used

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220

ls

cat readme
```

---

## Explanation

- Connected to the Bandit server using SSH.
- Listed the available files in the home directory.
- Located the `readme` file.
- Displayed its contents using the `cat` command to obtain the password for the next level.

---

## Commands Learned

| Command | Purpose |
|---------|----------|
| `ssh` | Establish a secure connection to a remote Linux machine |
| `ls` | List files and directories |
| `cat` | Display the contents of a file |

---

## Key Learning

- Introduction to Secure Shell (SSH).
- Basic Linux file enumeration.
- Reading file contents from the command line.

---

## Real-World Application

SSH is the standard protocol used by system administrators, DevOps engineers, cloud engineers, and cybersecurity professionals to securely access and manage remote Linux servers.

---

## Skills Practiced

- Linux
- SSH
- File Enumeration
- Command Line
