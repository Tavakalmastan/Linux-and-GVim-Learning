# Day 05 - File Searching, Comparison and Analysis Commands

## Objective

Today's learning focused on Linux commands used for searching files, comparing file contents, and analyzing text data efficiently.

---

## Topics Covered

### 1. find Command

The `find` command is used to search for files and directories recursively based on specified criteria.

#### Common Usage

```bash
find . -name "*.txt"
find . -type f
find . -type d
find . -size +100M
find . -mtime -7
find . -perm 644
find . -name "*.log" -exec rm {} \;
```

#### Important Options

| Option    | Description                 |
| --------- | --------------------------- |
| `-name`   | Search by file name         |
| `-type f` | Search only files           |
| `-type d` | Search only directories     |
| `-size`   | Search by file size         |
| `-mtime`  | Search by modification time |
| `-perm`   | Search by permissions       |
| `-exec`   | Execute command on results  |

#### Key Learnings

* Searches recursively inside subdirectories.
* Can filter results using multiple criteria.
* Useful for locating files quickly.
* Can execute commands directly on matched files.

---

### 2. File Comparison Commands

Linux provides several commands to compare files and identify differences.

---

#### diff Command

Compares two text files line by line.

```bash
diff file1.txt file2.txt
diff -u file1.txt file2.txt
diff -y file1.txt file2.txt
diff -q file1.txt file2.txt
```

##### Common Options

| Option | Description             |
| ------ | ----------------------- |
| `-u`   | Unified output format   |
| `-y`   | Side-by-side comparison |
| `-q`   | Brief comparison        |
| `-w`   | Ignore whitespace       |
| `-i`   | Ignore case differences |

##### Uses

* Review changes in files.
* Compare configuration files.
* Compare source code versions.

---

#### cmp Command

Compares files byte by byte and reports the first difference.

```bash
cmp file1.txt file2.txt
cmp -l file1.txt file2.txt
cmp -s file1.txt file2.txt
```

##### Common Options

| Option | Description              |
| ------ | ------------------------ |
| `-l`   | Show all differing bytes |
| `-s`   | Silent comparison        |
| `-n`   | Compare first N bytes    |

##### Uses

* Verify copied files.
* Check file integrity.
* Detect binary file differences.

---

#### comm Command

Compares two sorted files line by line.

```bash
comm file1.txt file2.txt
comm -1 file1.txt file2.txt
comm -2 file1.txt file2.txt
comm -3 file1.txt file2.txt
```

##### Common Options

| Option | Description       |
| ------ | ----------------- |
| `-1`   | Suppress column 1 |
| `-2`   | Suppress column 2 |
| `-3`   | Suppress column 3 |

##### Uses

* Find common entries.
* Find unique lines in files.
* Compare lists and reports.

---

#### sdiff Command

Displays differences side by side.

```bash
sdiff file1.txt file2.txt
```

##### Uses

* Easy visual comparison.
* Compare files during reviews.
* Merge file changes manually.

---

### 3. wc Command

The `wc` command counts lines, words, characters, and bytes in files.

#### Common Usage

```bash
wc file.txt
wc -l file.txt
wc -w file.txt
wc -c file.txt
wc -m file.txt
wc -L file.txt
```

#### Common Options

| Option | Description         |
| ------ | ------------------- |
| `-l`   | Count lines         |
| `-w`   | Count words         |
| `-c`   | Count bytes         |
| `-m`   | Count characters    |
| `-L`   | Longest line length |

#### Uses

* Count lines in log files.
* Count words in documents.
* Measure file size information.
* Analyze text files quickly.

---


## Summary

Today I learned how to search files using the `find` command, compare files using `diff`, `cmp`, `comm`, and `sdiff`, and analyze text data using the `wc` command. These commands are commonly used in Linux administration, debugging, file management, and automation tasks.
