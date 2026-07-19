# Bandit Level 5 → 6

## Objective

Retrieve the password for Bandit Level 6 by locating a file that matches specific search criteria.

---

## Challenge Description

The password for the next level is stored in a file somewhere under the `inhere` directory. The file has the following properties:

- Human-readable
- 1033 bytes in size
- Not executable

The challenge is to efficiently locate the correct file instead of manually inspecting every file.

---

## Enumeration

The `inhere` directory contained multiple subdirectories with numerous files. Manually checking each file would be inefficient, so I used the `find` command to filter files based on the required attributes.

---

## Commands Used

```bash
cd inhere

find . -type f -size 1033c ! -executable

cat ./maybehere07/.file2
```

> **Note:** The final file path may vary depending on the challenge version. Use the path returned by the `find` command.

---

## Explanation

- Navigated to the `inhere` directory.
- Used the `find` command to search recursively.
- Filtered the results to include only:
  - Regular files (`-type f`)
  - Files exactly 1033 bytes in size (`-size 1033c`)
  - Files that are not executable (`! -executable`)
- Opened the matching file using `cat` to retrieve the password.

---

## Commands Learned

| Command | Purpose |
|---------|----------|
| `find` | Search for files and directories based on specified conditions |
| `-type f` | Search only for regular files |
| `-size 1033c` | Match files exactly 1033 bytes in size |
| `! -executable` | Exclude executable files |
| `cat` | Display the contents of a file |

---

## Key Learning

- The `find` command is one of the most powerful Linux utilities for locating files.
- Combining multiple search filters significantly reduces search time.
- Automation and filtering are far more efficient than manual inspection.

---

## Real-World Application

System administrators and cybersecurity professionals frequently use the `find` command to locate log files, configuration files, suspicious executables, world-writable files, or recently modified files during system audits and incident response investigations.

---

## Skills Practiced

- Linux
- File Enumeration
- Recursive Searching
- Command Line
- Search Filtering
