# Bandit Level 6 → 7

## Objective

Retrieve the password for Bandit Level 7 by locating a file on the system that matches specific ownership and size requirements.

---

## Challenge Description

The password for the next level is stored somewhere on the server. The target file has the following properties:

- Owned by user `bandit7`
- Owned by group `bandit6`
- Exactly 33 bytes in size

The challenge is to efficiently search the entire filesystem while handling permission-related errors.

---

## Enumeration

Since the file was not located in the home directory, I searched the entire filesystem using the `find` command with the given criteria. During the search, many directories generated permission denied messages because the current user lacked access. These messages were redirected to `/dev/null` to keep the output focused on the valid search results.

---

## Commands Used

```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null

cat /var/lib/dpkg/info/<filename>
```

> **Note:** Replace `<filename>` with the file returned by the `find` command.

---

## Explanation

- Started searching from the root (`/`) directory.
- Filtered files by:
  - Owner (`-user bandit7`)
  - Group (`-group bandit6`)
  - Size (`-size 33c`)
- Redirected standard error (`2>`) to `/dev/null` to suppress permission denied messages.
- Opened the discovered file using `cat` to retrieve the password.

---

## Commands Learned

| Command | Purpose |
|---------|----------|
| `find /` | Search the entire filesystem |
| `-user` | Match files owned by a specific user |
| `-group` | Match files belonging to a specific group |
| `2>` | Redirect standard error |
| `/dev/null` | Discard unwanted output |
| `cat` | Display the contents of a file |

---

## Key Learning

- The `find` command supports filtering by ownership, permissions, and size.
- Linux separates standard output and standard error into different streams.
- Redirecting unnecessary error messages improves readability and efficiency.

---

## Real-World Application

Security analysts and system administrators frequently search systems for files owned by specific users, service accounts, or privileged groups. Redirecting error output is a common technique during audits and incident response to produce cleaner, more useful results without losing important information.

---

## Skills Practiced

- Linux
- File Enumeration
- File Ownership
- Output Redirection
- Command Line
