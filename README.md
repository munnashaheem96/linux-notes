
# Linux Basics

## 1. pwd – Present Working Directory

`pwd` stands for **Present Working Directory**.

It is used to display the absolute path of the current working directory.

**Command:**
```bash
pwd
```

**Example Output:**
```bash
/home/username
```

## 2. Linux Terminal Prompt Structure

```text
<username>@<machinename>:<default-location>$
```

**Definitions:**

- `<username>` – Current logged-in user's name.
- `<machinename>` – Computer's hostname.
- `<default-location>` – Current working directory.
- `$` – Indicates a normal user.
- `#` – Indicates a root (administrator) user.

## 3. ~ (Home Directory)

`~` represents the home directory of the currently logged-in user.

**Example:**
```bash
cd ~
```

This command takes you to your home directory.

If the username is `munna`, the home directory is usually:

```bash
/home/munna
```

## 4. Linux File System

The Linux file system follows a hierarchical directory structure, starting from the root directory `/`.

![Linux File System](linux-file-system.png)

**Image:** `linux-file-system.png`

