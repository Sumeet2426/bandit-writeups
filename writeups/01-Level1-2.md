# Bandit Level 1 → 2

## Objective

Retrieve the password for Bandit Level 2 from a file whose name contains a special character.

---

## Challenge Description

The password for the next level is stored in a file named `-`. Since `-` is commonly interpreted as standard input or an option by many Linux commands, the challenge is to access the file correctly.

---

## Enumeration

After listing the files in the current directory, I found a file named `-`. Attempting to read it directly caused the shell to interpret it as an option rather than a filename.

---

## Commands Used

```bash
ls

cat ./-
```

---

## Explanation

- Listed the files in the current directory.
- Identified a file named `-`.
- Used `./-` to explicitly specify that `-` is a file located in the current directory.
- Displayed the file's contents to retrieve the password for the next level.

---

## Commands Learned

| Command | Purpose |
|---------|----------|
| `ls` | List files and directories |
| `cat` | Display the contents of a file |
| `./` | Refer to a file in the current working directory |

---

## Key Learning

- Some filenames can conflict with command-line options.
- Prefixing a filename with `./` removes ambiguity by explicitly referencing the current directory.
- Understanding how the shell interprets command arguments is essential when working with unusual filenames.

---

## Real-World Application

Attackers or poorly designed applications may create files with unusual names to confuse administrators or automated scripts. Security professionals must know how to safely access and analyze such files without misinterpreting them as command options.

---

## Skills Practiced

- Linux
- Command Line
- File Handling
- Special Filenames
