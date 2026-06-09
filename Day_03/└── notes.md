# Day 03 - Linux Fundamentals and File Management

## Objective

Started learning Linux fundamentals, understanding Bash Shell, Linux command syntax, file system navigation, file management commands, and input/output redirection.

---

# Introduction to Linux

Linux is a powerful open-source operating system widely used in:

- Servers
- Cloud Computing
- Embedded Systems
- VLSI and EDA Tools
- Software Development
- Automation

---

# Bash Shell

Bash (Bourne Again Shell) is the default command-line interpreter in Linux.

## Workflow

1. User enters command
2. Bash interprets the command
3. Bash interacts with:
   - File System
   - Processes
   - Kernel
4. Output is displayed in terminal

---

# Linux Command Syntax

General format:

```bash
command [options] [arguments]
```

## Example

```bash
ls -l /home/user
```

Where:

- ls → command
- -l → option
- /home/user → argument

---

# Basic Linux Commands

## pwd

Print Working Directory.

```bash
pwd
```

Displays the current directory path.

Example:

```bash
/home/user/projects
```

---

## ls

Lists files and directories.

### Common Variations

```bash
ls
ls -l
ls -a
ls -la
ls -R
ls -lh
ls -lt
ls -lS
```

### Purpose

| Command | Description |
|----------|------------|
| ls | List files |
| ls -l | Long listing |
| ls -a | Show hidden files |
| ls -la | Long + hidden |
| ls -R | Recursive listing |
| ls -lh | Human-readable size |
| ls -lt | Sort by time |
| ls -lS | Sort by size |

---

# Linux File Type Indicators

| Symbol | File Type |
|----------|------------|
| - | Regular File |
| d | Directory |
| l | Symbolic Link |
| c | Character Device |
| b | Block Device |
| p | Named Pipe |
| s | Socket |

---

# cd Command

Used to change directories.

## Commands

```bash
cd directory
cd ..
cd ~
cd /
cd -
```

### Description

| Command | Purpose |
|----------|----------|
| cd dir | Enter directory |
| cd .. | Parent directory |
| cd ~ | Home directory |
| cd / | Root directory |
| cd - | Previous directory |

---

# touch Command

Used to create empty files or update timestamps.

## Examples

```bash
touch file1.txt
touch file1.txt file2.txt
touch test.log
```

Create multiple files:

```bash
touch file1 file2 file3
```

---

# mkdir Command

Used to create directories.

## Examples

```bash
mkdir mydir
mkdir dir1 dir2 dir3
mkdir -p project/src/docs
```

### Useful Option

```bash
mkdir -p
```

Creates parent directories automatically.

---

# Remove Commands

## Remove File

```bash
rm file.txt
```

## Remove Empty Directory

```bash
rmdir empty_dir
```

## Remove Multiple Files

```bash
rm *.txt
```

---

# Copy Command (cp)

Used to copy files and directories.

## Examples

```bash
cp file1.txt file2.txt
cp file.txt backup/
cp -r project backup/
```

### Common Options

| Option | Description |
|----------|------------|
| -r | Recursive copy |
| -i | Confirm before overwrite |
| -v | Verbose mode |
| -p | Preserve attributes |

---

# Move / Rename Command (mv)

Used to move or rename files.

## Rename File

```bash
mv oldname.txt newname.txt
```

## Move File

```bash
mv file.txt folder/
```

## Move Directory

```bash
mv project backup/
```

---

# Input / Output Redirection

## Overwrite Output

```bash
ls > files.txt
```

---

## Append Output

```bash
date >> log.txt
```

---

## Input Redirection

```bash
sort < names.txt
```

---

## Redirect Errors

```bash
ls wrongfile 2> error.txt
```

---

# Key Concepts Learned

- Linux Command Structure
- Bash Shell Working
- File System Navigation
- File Management Commands
- Linux File Types
- Input and Output Redirection
- Directory Operations
- Copy, Move and Delete Operations

---

# Practice Performed

- Navigated directories using cd
- Checked current path using pwd
- Listed files using ls
- Created files using touch
- Created directories using mkdir
- Deleted files using rm
- Copied files using cp
- Renamed files using mv
- Practiced output redirection

---

# Key Takeaways

- Linux commands follow a standard syntax.
- Bash acts as the interface between user and operating system.
- File and directory management is performed using command-line tools.
- Redirection helps save command output into files.
- Understanding Linux is essential for VLSI and EDA workflows.

