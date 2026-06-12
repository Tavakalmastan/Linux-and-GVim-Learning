# Day 06 - File Searching and Permission Management in Linux

## Objective

Today's learning focused on advanced file searching using the `find` command and managing file permissions using the `chmod` command.

---

## Topics Covered

### 1. Find Command

The `find` command is used to search files and directories recursively based on different conditions.

#### Find Files by Name

```bash
find . -name "file1.txt"
find . -name "*.txt"
find . -name "file.*"
```

#### Find Files and Directories

```bash
find . -type f
find . -type d
```

#### Find Based on Time

```bash
find . -cmin -30
find . -ctime -1
find . -mtime -7
```

#### Find Empty Files and Directories

```bash
find . -empty
find . -type f -empty
find . -type d -empty
```

#### Execute Commands Using find

```bash
find . -name "*.txt" -exec ls -l {} \;
find . -name "*.txt" -exec wc {} \;
```

#### Other Useful Options

```bash
find . -size +100M
find . -perm 755
find . -user username
find . -delete
```

---

### 2. Linux File Permissions

Linux permissions control access to files and directories.

#### User Categories

- User (u)
- Group (g)
- Others (o)

#### Permission Types

- Read (r)
- Write (w)
- Execute (x)

---

### 3. chmod Command

Used to modify file permissions.

#### Symbolic Method

```bash
chmod u+x file.sh
chmod g-w file.txt
chmod o+r file.txt
chmod u-rwx file.txt
```

#### Numeric Method

```bash
chmod 777 file.txt
chmod 755 script.sh
chmod 644 notes.txt
chmod 700 private.sh
chmod 750 linux.tcl
```

---

## Common Permission Values

| Value | Permission |
|---------|-----------|
| 777 | rwxrwxrwx |
| 755 | rwxr-xr-x |
| 644 | rw-r--r-- |
| 700 | rwx------ |
| 750 | rwxr-x--- |
| 600 | rw------- |

---

## Practice Performed

### File Creation

```bash
touch file{1..20}.txt
touch file.v file.py file.tcl file.pdf
mkdir folder
```

### File Search Practice

```bash
find . -name "file*.txt" -type f
find . -name "file.*" -type f
find . -name "folder*" -type d
```

### Time-Based Search

```bash
find . -cmin -30
find . -ctime -1
```

### Command Execution with find

```bash
find . -name "*.txt" -exec ls -l {} \;
find . -name "*.txt" -exec wc {} \;
```

### Empty File Detection

```bash
find . -empty
```

### Permission Modification Practice

```bash
chmod u-rwx,g+rwx,o-rwx file.v
chmod 777 linux.tcl
chmod 750 linux.tcl
chmod 656 linux.tcl
chmod 451 linux.tcl
```

### System Information Commands

```bash
whoami
hostname
who
```

---

## Key Learnings

- Learned advanced usage of the `find` command.
- Practiced searching files using name, type, size, and time filters.
- Executed commands on search results using `-exec`.
- Understood Linux permission structure.
- Practiced both symbolic and numeric permission methods.
- Learned commonly used permission values for files and scripts.

