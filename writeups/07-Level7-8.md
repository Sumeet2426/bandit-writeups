# Bandit Level 7 → 8

## Objective

Retrieve the password for Bandit Level 8 by locating a specific line within a data file.

---

## Challenge Description

The password for the next level is stored in the file `data.txt` next to the word `millionth`. The challenge is to efficiently search the file for the matching line.

---

## Enumeration

After listing the files in the current directory, I found `data.txt`. Since the file contained a large amount of text, manually searching through it would be inefficient. Instead, I used the `grep` command to search for the required keyword.

---

## Commands Used

```bash
ls

grep "millionth" data.txt
```

---

## Explanation

- Listed the files in the current directory.
- Identified the file `data.txt`.
- Used `grep` to search for the line containing the keyword `millionth`.
- Retrieved the password from the matching line.

---

## Commands Learned

| Command | Purpose |
|---------|----------|
| `grep` | Search for lines matching a specific pattern |
| `ls` | List files and directories |

---

## Key Learning

- The `grep` command is one of the most useful Linux text-processing utilities.
- Searching by pattern is much faster and more reliable than manually reading large files.
- Efficient text searching is an essential skill for working with logs and configuration files.

---

## Real-World Application

Security analysts regularly use `grep` to search through log files for indicators of compromise (IOCs), failed login attempts, suspicious IP addresses, malware signatures, or error messages. It is a fundamental tool in incident response, digital forensics, and system administration.

---

## Skills Practiced

- Linux
- Text Processing
- Pattern Matching
- Command Line
- File Enumeration
