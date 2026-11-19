
# Linux Basics

## 1. pwd – Present Working Directory

`pwd` stands for **Present Working Directory**.

It displays the absolute path of the current working directory.

```bash
pwd
```

**Example Output:**
```text
/home/munna
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

```bash
cd ~
```

Example:
```text
/home/munna
```

## 4. Linux File System

The Linux file system follows a hierarchical directory structure, starting from the root directory `/`.

![Linux File System](linux-file-system.png)

Image: `linux-file-system.png`

---

# Basic Linux Commands

## 5. ls – List Directory Contents

Displays files and directories in the current directory.

```bash
ls
```

Useful options:
```bash
ls -l       # Detailed listing
ls -a       # Show hidden files
ls -lh      # Human-readable file sizes
ls -la      # Detailed listing including hidden files
```

## 6. pwd – Present Working Directory

Displays the current directory's absolute path.

```bash
pwd
```

## 7. mkdir – Make Directory

Creates a new directory.

```bash
mkdir foldername
```

Example:
```bash
mkdir Linux
```

Create multiple directories:
```bash
mkdir folder1 folder2 folder3
```

## 8. rmdir – Remove Directory

Removes an empty directory.

```bash
rmdir foldername
```

Example:
```bash
rmdir Linux
```

Note: `rmdir` only removes empty directories.

## 9. touch – Create File

Creates an empty file if it does not exist.

```bash
touch filename
```

Example:
```bash
touch notes.txt
```

Create multiple files:
```bash
touch file1.txt file2.txt file3.txt
```

## 10. mv – Move or Rename Files

Used to move files/directories or rename them.

**Rename a file:**
```bash
mv oldname.txt newname.txt
```

**Move a file into another directory:**
```bash
mv file.txt Documents/
```

**Move a directory:**
```bash
mv folder1 Documents/
```

## 11. cp – Copy Files and Directories

Used to copy files and directories.

**Copy a file:**
```bash
cp file.txt backup.txt
```

**Copy a file into another directory:**
```bash
cp file.txt Documents/
```

**Copy a directory recursively:**
```bash
cp -r folder1 folder2
```

---

## Quick Reference

| Command | Description |
|---|---|
| `pwd` | Display current directory |
| `ls` | List files and directories |
| `mkdir` | Create a directory |
| `rmdir` | Remove an empty directory |
| `touch` | Create an empty file |
| `mv` | Move or rename files |
| `cp` | Copy files and directories |
