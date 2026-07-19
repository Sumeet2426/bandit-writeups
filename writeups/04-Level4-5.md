# Bandit Level 4 → 5

## Objective

Retrieve the password for Bandit Level 5 from the only human-readable file located inside the `inhere` directory.

---

## Challenge Description

The password for the next level is stored in the only human-readable file among several files in the `inhere` directory. The challenge is to identify which file contains readable text before viewing its contents.

---

## Enumeration

After entering the `inhere` directory, I listed all the files and noticed multiple files with similar names. Instead of opening each file manually, I used the `file` command to determine the type of every file and identify the human-readable one.

---

## Commands Used

```bash
cd inhere

ls -a

file ./*

cat ./-file07
```

> **Note:** The human-readable filename (e.g., `-file07`) may differ depending on the challenge version. Replace it with the file identified by the `file` command.

---

## Explanation

- Navigated to the `inhere` directory.
- Listed the available files.
- Used the `file` command to inspect the type of each file.
- Identified the only ASCII text (human-readable) file.
- Displayed its contents using `cat` to retrieve the password for the next level.

---

## Commands Learned

| Command | Purpose |
|---------|----------|
| `file` | Determine the type of a file based on its contents |
| `cat` | Display the contents of a file |
| `./*` | Match all files in the current directory |

---

## Key Learning

- File extensions are not always reliable indicators of a file's content.
- The `file` command identifies files by examining their contents rather than their names.
- Enumeration tools help locate relevant files quickly and efficiently.

---

## Real-World Application

Security professionals frequently use the `file` command during malware analysis, digital forensics, and incident response to identify unknown files. Since attackers often disguise malicious files with misleading names or extensions, checking the actual file type is an essential investigative step.

---

## Skills Practiced

- Linux
- File Enumeration
- File Identification
- Command Line
