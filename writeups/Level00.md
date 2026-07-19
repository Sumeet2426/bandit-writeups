# Bandit Level 0 → 1

## Objective

Connect to the Bandit server using SSH and retrieve the password for Bandit Level 1.

---

## Challenge Description

The goal of this level is to establish a remote SSH connection and read the contents of a file containing the password for the next level.

---

## Enumeration

After connecting to the remote machine, I listed the files in the home directory to identify any useful information.

---

## Commands Used

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220

ls

cat readme
```

---

## Explanation

- Connected securely to the Bandit server using SSH.
- Listed the files available in the home directory.
- Found a file named `readme`.
- Displayed its contents using the `cat` command to obtain the password for the next level.

---

## Commands Learned

| Command | Description |
|----------|-------------|
| `ssh` | Securely connect to a remote Linux machine |
| `ls` | Display files and directories |
| `cat` | Display file contents |

---

## Key Learning

- Introduction to SSH.
- Basic Linux navigation.
- Reading file contents from the terminal.

---

## Real-World Application

SSH is the standard protocol used by Linux administrators, cloud engineers, and cybersecurity professionals for secure remote administration of servers.

---

## Skills Practiced

- Linux
- SSH
- Enumeration
- Command Line
