# Bandit Level 8 → 9

## Objective

Retrieve the password for Bandit Level 9 by identifying the only unique line in a data file.

---

## Challenge Description

The password for the next level is stored in the file `data.txt` and is the only line that occurs exactly once. Every other line appears multiple times.

---

## Enumeration

After locating `data.txt`, I needed to identify the line that appeared only once. Since manually counting repeated lines would be inefficient, I used a combination of Linux text-processing utilities to sort the data and find the unique entry.

---

## Commands Used

```bash
sort data.txt | uniq -u
```

---

## Explanation

- Used `sort` to arrange all lines alphabetically.
- Piped (`|`) the sorted output to the `uniq` command.
- The `-u` option displayed only lines that appeared exactly once.
- The resulting unique line was the password for the next level.

---

## Commands Learned

| Command | Purpose |
|---------|----------|
| `sort` | Sort lines of text alphabetically or numerically |
| `uniq` | Filter or report repeated lines |
| `uniq -u` | Display only unique lines |
| `|` (Pipe) | Pass the output of one command as the input to another |

---

## Key Learning

- Some Linux commands depend on the output format of previous commands.
- The `uniq` command only detects consecutive duplicate lines, making `sort` an important preprocessing step.
- Combining small commands using pipes is a core principle of the Unix philosophy.

---

## Real-World Application

Security professionals frequently combine commands with pipes to analyze logs, identify unique IP addresses, detect duplicate events, and process large datasets efficiently. Building command pipelines is an essential skill for incident response, threat hunting, and system administration.

---

## Skills Practiced

- Linux
- Text Processing
- Data Filtering
- Command Pipelines
- Command Line
