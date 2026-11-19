
# Linux Basics – Complete Notes

Beginner-friendly Linux commands, file system concepts, searching, text processing and practical examples.

---

# 1. Linux Basics

## 1.1 pwd – Present Working Directory

`pwd` stands for **Present Working Directory**.

It displays the absolute path of the current working directory.

**Command:**

```bash
pwd
```

**Example Output:**

```text
/home/munna
```

## 1.2 Linux Terminal Prompt Structure

A common Linux terminal prompt looks like this:

```text
<username>@<machinename>:<default-location>$
```

**Definitions:**

- `<username>` – Name of the currently logged-in user.
- `<machinename>` – Hostname of the computer.
- `<default-location>` – Current working directory.
- `$` – Indicates a normal user shell.
- `#` – Commonly indicates a root (administrator) shell.

The exact prompt format can vary depending on the shell configuration.

## 1.3 ~ – Home Directory

The tilde (`~`) represents the home directory of the currently logged-in user.

**Command:**

```bash
cd ~
```

Example:

```text
/home/munna
```

## 1.4 Linux File System

The Linux file system follows a hierarchical directory structure starting from the root directory `/`.

![Linux File System](linux-file-system.png)

**Image:** `linux-file-system.png`

Keep the image in the same folder as this README file.

---

# 2. Basic Linux Commands

## 2.1 ls – List Directory Contents

Displays files and directories in the current directory.

```bash
ls
```

**Useful options:**

```bash
ls -l       # Detailed listing
ls -a       # Show hidden files
ls -lh      # Human-readable file sizes
ls -la      # Detailed listing including hidden files
```

## 2.2 pwd – Present Working Directory

Displays the absolute path of the current directory.

```bash
pwd
```

## 2.3 mkdir – Make Directory

Creates a new directory.

```bash
mkdir foldername
```

**Example:**

```bash
mkdir Linux
```

Create multiple directories:

```bash
mkdir folder1 folder2 folder3
```

## 2.4 rmdir – Remove Directory

Removes an empty directory.

```bash
rmdir foldername
```

**Example:**

```bash
rmdir Linux
```

Note: `rmdir` only removes empty directories.

## 2.5 touch – Create File

Creates an empty file if it does not exist. If the file already exists, it updates its timestamps.

```bash
touch filename.txt
```

**Example:**

```bash
touch notes.txt
```

Create multiple files:

```bash
touch file1.txt file2.txt file3.txt
```

## 2.6 mv – Move or Rename Files

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

## 2.7 cp – Copy Files and Directories

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

## 2.8 rm – Remove Files and Directories

Removes files and directories.

**Remove a file:**

```bash
rm file.txt
```

**Remove a directory and its contents:**

```bash
rm -r foldername
```

**Force removal:**

```bash
rm -f file.txt
```

Be careful: deleted files may not go to a recycle bin.

## 2.9 date – Display Date and Time

Displays the current system date and time.

```bash
date
```

---

# 3. Command Concepts

## 3.1 What is a Command?

A command is a program or shell instruction that performs a specific operation when executed.

## 3.2 Flags

Flags are usually specified using `-` or `--`.

They are used to change the normal behaviour of a command.

**Examples:**

```bash
ls -l
ls -a
ls --all
```

## 3.3 Parameters

A parameter is a value passed to a command for processing.

**Example:**

```bash
mkdir Linux
```

Here, `Linux` is the parameter.

---

# 4. Getting Information About Commands

## 4.1 man – Manual Pages

Displays the manual page of a command.

```bash
man ls
```

## 4.2 info – Information Pages

Displays detailed documentation when an Info page is available.

```bash
info
```

## 4.3 help – Shell Built-in Help

Displays help information for shell built-in commands.

```bash
help
help cd
```

---

# 5. Searching Commands and Files

## 5.1 find – Local Search

Used to search for files and directories within a specified location.

**Search by filename:**

```bash
find . -name "file.txt"
```

**Search for all files:**

```bash
find /home -type f
```

**Search for directories:**

```bash
find /home -type d
```

## 5.2 locate – File Search

Used to search for file paths using a prebuilt filename database.

```bash
locate file.txt
```

Note: Results depend on how recently the filename database was updated.

## 5.3 whereis – Software Search

Used to locate the binary, source and manual page files of a command.

```bash
whereis ls
```

## 5.4 which – Command Location

Used to locate an executable through the shell's PATH.

```bash
which python
which ls
```

## 5.5 grep – Pattern Searching

Used to search for specific text patterns inside files or input.

```bash
grep "Linux" file.txt
```

**Useful options:**

```bash
grep -i "linux" file.txt    # Case-insensitive search
grep -n "Linux" file.txt    # Display line numbers
grep -v "Linux" file.txt    # Display non-matching lines
grep -r "Linux" folder/     # Search recursively
```

---

# 6. Working with Text Files – cat

`cat` is used to display file contents. With shell redirection, it can also create and append text files.

## 6.1 Read a File

```bash
cat filename.txt
```

Displays the contents of the file.

## 6.2 Create a File

```bash
cat > filename.txt
```

Creates a new file or overwrites an existing file with entered content.

Press `Ctrl + D` to finish entering content.

## 6.3 Append Content

```bash
cat >> filename.txt
```

Adds content to the end of an existing file without deleting its previous content.

Press `Ctrl + D` to finish.

## 6.4 Display Multiple Files

```bash
cat file1.txt file2.txt
```

Displays the contents of multiple files.

---

# 7. vi / vim Editor

`vi` and `vim` are terminal-based text editors used to create and modify files.

**Open a file:**

```bash
vi filename.txt
```

Or:

```bash
vim filename.txt
```

## Basic Vim Operations

| Key | Function |
|---|---|
| `i` | Enter insert mode |
| `Esc` | Return to normal mode |
| `:w` | Save the file |
| `:q` | Quit |
| `:wq` | Save and quit |
| `:q!` | Quit without saving changes |

---

# 8. Sorting – sort

`sort` is used to arrange lines of text in a particular order.

By default, it sorts in ascending order according to the current locale.

## 8.1 Normal Sorting

```bash
sort filename.txt
```

Displays the content in sorted order.

## 8.2 Reverse Sorting

```bash
sort -r filename.txt
```

Displays the content in reverse sorted order.

## 8.3 Numeric Sorting

```bash
sort -n numbers.txt
```

Sorts numbers numerically instead of alphabetically.

## 8.4 Unique Sorting

```bash
sort -u filename.txt
```

Sorts the content and removes duplicate lines.

Note: `sort` does not modify the original file unless the output is redirected.

---

# 9. AWK – Text Processing Tool

## 9.1 What is AWK?

AWK is a powerful Linux command-line tool used for text processing, pattern scanning and data extraction.

It is commonly used to:

- Read text files.
- Extract specific columns.
- Search for patterns.
- Filter data using conditions.
- Perform mathematical calculations.
- Process log files.
- Format output.

**Example:**

Consider a file named `students.txt`:

```text
Munna 21 85
Aseeb 22 90
Sinan 21 75
```

Display only student names:

```bash
awk '{print $1}' students.txt
```

**Output:**

```text
Munna
Aseeb
Sinan
```

## 9.2 Basic AWK Syntax

```bash
awk 'pattern { action }' filename
```

**Definitions:**

- `awk` – Command used for text processing.
- `pattern` – Condition to check.
- `{ }` – Contains the action.
- `action` – Operation to perform.
- `filename` – Input file.

## 9.3 Understanding AWK Fields

AWK automatically divides each line into fields (columns).

Consider this file:

```text
Munna 21 85
Aseeb 22 90
Sinan 21 75
```

Field representation:

```text
Munna    21    85
  $1     $2    $3
```

**Important field references:**

| Field | Meaning |
|---|---|
| `$0` | Entire current line |
| `$1` | First field |
| `$2` | Second field |
| `$3` | Third field |
| `$NF` | Last field |

**Examples:**

```bash
awk '{print $1}' students.txt
awk '{print $2}' students.txt
awk '{print $3}' students.txt
awk '{print $0}' students.txt
awk '{print $NF}' students.txt
```

## 9.4 AWK Built-in Variables

AWK provides predefined variables that help process text.

| Variable | Meaning |
|---|---|
| `$0` | Entire current line |
| `$1` | First field |
| `$2` | Second field |
| `NF` | Number of fields in current record |
| `NR` | Current record number |
| `FS` | Input field separator |
| `OFS` | Output field separator |
| `RS` | Input record separator |
| `ORS` | Output record separator |
| `FNR` | Record number within the current file |

### NR – Record Number

Displays the current line number.

```bash
awk '{print NR, $0}' students.txt
```

**Output:**

```text
1 Munna 21 85
2 Aseeb 22 90
3 Sinan 21 75
```

### NF – Number of Fields

Displays the number of fields in each line.

```bash
awk '{print NF}' students.txt
```

**Output:**

```text
3
3
3
```

## 9.5 Printing Multiple Columns

You can print multiple fields using AWK.

```bash
awk '{print $1, $3}' students.txt
```

**Output:**

```text
Munna 85
Aseeb 90
Sinan 75
```

Print with custom text:

```bash
awk '{print "Name:", $1, "Mark:", $3}' students.txt
```

## 9.6 AWK with Conditions

AWK can filter data using conditions.

**Example: Display students whose marks are greater than 80.**

```bash
awk '$3 > 80 {print $1, $3}' students.txt
```

**Output:**

```text
Munna 85
Aseeb 90
```

### Comparison Operators

| Operator | Meaning |
|---|---|
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal |
| `<=` | Less than or equal |
| `==` | Equal to |
| `!=` | Not equal to |
| `&&` | Logical AND |
| `||` | Logical OR |

**Examples:**

```bash
awk '$3 >= 80 {print $1}' students.txt

awk '$2 == 21 {print $1}' students.txt

awk '$3 < 80 {print $1}' students.txt

awk '$2 == 21 && $3 > 80 {print $1}' students.txt
```

## 9.7 AWK with Field Separators – FS

By default, AWK separates fields using whitespace (spaces or tabs).

Sometimes data uses commas, colons or other separators.

Consider `students.csv`:

```csv
Munna,21,85
Aseeb,22,90
Sinan,21,75
```

To read comma-separated values:

```bash
awk -F',' '{print $1}' students.csv
```

**Output:**

```text
Munna
Aseeb
Sinan
```

Here:

- `-F` specifies the input field separator.
- `','` means comma-separated data.

**Other examples:**

```bash
awk -F':' '{print $1}' /etc/passwd

awk -F',' '{print $1, $2}' students.csv

awk -F'|' '{print $1}' data.txt
```

## 9.8 BEGIN and END Blocks

AWK has two special blocks:

- `BEGIN` – Executes once before processing input records.
- `END` – Executes once after processing all input records.

**Example:**

```bash
awk 'BEGIN {print "Student Details"}
{print $1, $3}
END {print "Processing Completed"}' students.txt
```

**Output:**

```text
Student Details
Munna 85
Aseeb 90
Sinan 75
Processing Completed
```

**Execution order:**

```text
BEGIN
  |
  v
Main Action (each input record)
  |
  v
END
```

## 9.9 AWK Arithmetic Operations

AWK supports mathematical operations.

| Operator | Operation |
|---|---|
| `+` | Addition |
| `-` | Subtraction |
| `*` | Multiplication |
| `/` | Division |
| `%` | Modulus |

Consider `marks.txt`:

```text
Munna 80
Aseeb 90
Sinan 70
```

### Calculate Total Marks

```bash
awk '{sum += $2} END {print sum}' marks.txt
```

**Output:**

```text
240
```

### Calculate Average Marks

```bash
awk '{sum += $2} END {print sum/NR}' marks.txt
```

**Output:**

```text
80
```

## 9.10 AWK Formatting – printf

`printf` is used to format output.

```bash
awk '{printf "Name: %-10s Mark: %d\n", $1, $3}' students.txt
```

**Formatting symbols:**

| Symbol | Meaning |
|---|---|
| `%s` | String |
| `%d` | Integer |
| `%f` | Floating-point number |
| `\n` | New line |
| `%-10s` | Left-aligned string in a 10-character field |

## 9.11 Practical AWK Examples

Assume `students.txt` contains:

```text
Munna 21 85
Aseeb 22 90
Sinan 21 75
```

| Requirement | Command |
|---|---|
| Display first column | `awk '{print $1}' students.txt` |
| Display last column | `awk '{print $NF}' students.txt` |
| Display first and third columns | `awk '{print $1,$3}' students.txt` |
| Display line numbers | `awk '{print NR,$0}' students.txt` |
| Display field count | `awk '{print NF}' students.txt` |
| Marks above 80 | `awk '$3>80' students.txt` |
| Display second line | `awk 'NR==2' students.txt` |
| Display first three lines | `awk 'NR<=3' students.txt` |
| Calculate total marks | `awk '{s+=$3} END {print s}' students.txt` |
| Count records | `awk 'END {print NR}' students.txt` |

## 9.12 Difference Between grep, sed and awk

| Command | Main Purpose |
|---|---|
| `grep` | Search text patterns |
| `sed` | Edit and transform text |
| `awk` | Extract, filter and process structured text |

All three are useful Linux text-processing tools.

## 9.13 AWK Quick Reference

```bash
awk '{print $1}' file.txt

awk '{print $NF}' file.txt

awk '{print NR, $0}' file.txt

awk '{print NF}' file.txt

awk -F',' '{print $1}' file.csv

awk '$2 > 50' file.txt

awk 'BEGIN {print "Start"} {print $0} END {print "End"}' file.txt
```

---

# 10. AWK Practice Exercises

Create a file named `students.txt`:

```text
Munna 21 85
Aseeb 22 90
Sinan 21 75
```

Try the following exercises:

1. Display only the first column.
2. Display only the last column.
3. Display line numbers with each record.
4. Display students scoring above 80.
5. Display students whose age is 21.
6. Count the total number of records.
7. Calculate the total marks.
8. Calculate the average marks.
9. Display only the second record.
10. Display the first and third columns.

---

# 11. Linux Commands – Quick Reference

| Command | Description |
|---|---|
| `pwd` | Display current directory |
| `ls` | List files and directories |
| `mkdir` | Create directory |
| `rmdir` | Remove empty directory |
| `touch` | Create empty file |
| `mv` | Move or rename files |
| `cp` | Copy files and directories |
| `rm` | Remove files and directories |
| `date` | Display date and time |
| `man` | Display manual pages |
| `info` | Display Info documentation |
| `help` | Display shell built-in help |
| `find` | Search for files and directories |
| `locate` | Search using filename database |
| `whereis` | Locate command files |
| `which` | Locate executable through PATH |
| `grep` | Search text patterns |
| `cat` | Display, create or append text |
| `vi` | Open text editor |
| `vim` | Open Vim text editor |
| `sort` | Sort text lines |
| `awk` | Process and extract text data |

---

# 12. Practice in WSL

Practice all these commands in your WSL terminal.

**Suggested practice directory:**

```bash
mkdir Linux-Practice

cd Linux-Practice

touch students.txt

cat > students.txt
Munna 21 85
Aseeb 22 90
Sinan 21 75
```

Press `Ctrl + D` to save the entered content.

Now try:

```bash
pwd

ls -l

cat students.txt

awk '{print $1}' students.txt

awk '$3 > 80 {print $1}' students.txt

sort students.txt
```

---

*Linux Learning Notes | Beginner to Intermediate*
