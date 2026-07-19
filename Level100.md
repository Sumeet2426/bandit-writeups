# Bandit Level 0 → 1

## Objective

Connect to the Bandit server and obtain the password for Bandit Level 1.

---

## Enumeration

- Connected to the server using SSH.
- Verified successful login.
- Listed files in the home directory.

---

## Commands Used

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
ls
cat readme
```

---

## Explanation

The password for the next level was stored inside the `readme` file. After connecting through SSH, I listed the files and displayed the contents of the file using the `cat` command.

---

## Commands Learned

| Command | Purpose |
|---------|----------|
| `ssh` | Connect to a remote machine |
| `ls` | List files |
| `cat` | Display file contents |

---

## Key Learning

- Connecting to a remote Linux machine using SSH.
- Basic Linux navigation.
- Reading file contents.

---

## Real-World Concept

SSH is the standard protocol used by system administrators and security professionals to securely access remote Linux servers.

---

## Skills Practiced

- SSH
- Linux CLI
- File Enumeration
