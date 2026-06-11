# Day 05 - File Searching, Comparison and Analysis Commands

## Objective

Today's learning focused on Linux commands used for searching files, comparing file contents, and analyzing text data efficiently.

---

## Topics Covered

### 1. find Command

Used to search files and directories recursively based on different criteria.

Common usage:

```bash
find . -name "*.txt"
find . -type f
find . -type d
find . -size +100M
find . -mtime -7
find . -perm 644
```

Key points:

- Search files by name
- Search files and directories separately
- Search by size, date, and permissions
- Perform operations on search results

---

### 2. File Comparison Commands

#### diff Command

Compares two files line by line.

```bash
diff file1.txt file2.txt
diff -u file1.txt file2.txt
diff -y file1.txt file2.txt
```

Used for:

- Finding changes between files
- Comparing configuration files
- Reviewing modifications

#### cmp Command

Compares two files byte by byte.

```bash
cmp file1.txt file2.txt
cmp -l file1.txt file2.txt
cmp -s file1.txt file2.txt
```

Used for:

- Checking if files are identical
- Detecting byte-level differences

#### comm Command

Compares two sorted files.

```bash
comm file1.txt file2.txt
comm -1 file1.txt file2.txt
comm -2 file1.txt file2.txt
comm -3 file1.txt file2.txt
```

Used for:

- Finding common lines
- Finding unique entries in files

---

### 3. wc Command

Used to count lines, words, characters, and bytes.

Common usage:

```bash
wc file.txt
wc -l file.txt
wc -w file.txt
wc -c file.txt
wc -m file.txt
wc -L file.txt
```

Useful for:

- Counting lines in files
- Counting words in documents
- Checking file size statistics
- Analyzing log files

---

## Commands Practiced

```bash
find . -name "*.txt"
find . -type f
find . -type d

diff file1.txt file2.txt
diff -u file1.txt file2.txt

cmp file1.txt file2.txt
cmp -l file1.txt file2.txt

comm file1.txt file2.txt

wc file.txt
wc -l file.txt
wc -w file.txt
wc -c file.txt
```

---

## Summary

Learned how to search files using the find command, compare files using diff, cmp, and comm, and analyze file contents using the wc command. These commands are useful for file management, troubleshooting, and text processing in Linux.
