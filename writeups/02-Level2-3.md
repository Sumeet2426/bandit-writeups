# Bandit Level 2 → 3

## Objective

Retrieve the password for Bandit Level 3 from a file whose name contains spaces.

---

## Challenge Description

The password for the next level is stored in a file named `spaces in this filename`. Since spaces are used by the shell to separate command arguments, the filename must be handled correctly.

---

## Enumeration

After listing the files in the current directory, I identified a file with multiple spaces in its name. Attempting to access it without proper formatting caused the shell to interpret each word as a separate argument.

---

## Commands Used

```bash
ls

cat "spaces in this filename"
```

Alternative:

```bash
cat spaces\ in\ this\ filename
```

---

## Explanation

- Listed the files in the current directory.
- Identified a filename containing spaces.
- Used double quotes to treat the entire filename as a single argument.
- Alternatively, escaped each space using a backslash (`\`).
- Displayed the file contents to retrieve the password for the next level.

---

## Commands Learned

| Command | Purpose |
|---------|----------|
| `ls` | List files and directories |
| `cat` | Display the contents of a file |
| `""` | Treat enclosed text as a single argument |
| `\` | Escape the special meaning of the following character |

---

## Key Learning

- The shell splits command-line arguments at spaces by default.
- Quoting or escaping spaces allows filenames with whitespace to be handled correctly.
- Understanding shell parsing helps avoid command errors and scripting issues.

---

## Real-World Application

Files and directories with spaces are common on user systems, shared drives, and Windows environments. Security professionals and system administrators must know how to correctly reference these paths while writing scripts, investigating systems, or transferring files.

---

## Skills Practiced

- Linux
- Command Line
- File Handling
- Shell Quoting
- Escape Characters
