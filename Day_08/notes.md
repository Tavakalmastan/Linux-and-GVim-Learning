# Day_08 - File Permissions, Pipes, Tee, Xargs and Regular Expressions

## Objective

Today's learning focused on Linux file access permissions, permission management commands, pipes, tee command, xargs command, and Regular Expressions (Regex) for advanced text processing and command chaining.

---

## Topics Covered

### 1. File Access Permissions in Linux

Linux provides three types of permissions for three categories of users.

User Categories:

- User (u)
- Group (g)
- Others (o)

Permission Types:

- Read (r) = 4
- Write (w) = 2
- Execute (x) = 1

Permission Example:

```bash
-rwxr-xr--
```

Numeric Representation:

| Permission | Value |
|------------|--------|
| r | 4 |
| w | 2 |
| x | 1 |

Common Permission Sets:

| Octal | Meaning |
|---------|---------|
| 777 | Full access for everyone |
| 755 | Owner full access, others read & execute |
| 700 | Owner only access |
| 644 | Read/write owner, read-only others |
| 600 | Owner read/write only |

Key Learnings:

- Linux permissions are divided into user, group and others.
- Permissions can be represented symbolically and numerically.
- Proper permissions improve system security.
- Least privilege principle should be followed.

---

### 2. chmod Command

Used to change file and directory permissions.

Syntax:

```bash
chmod [permissions] file
```

Numeric Mode:

```bash
chmod 755 file.txt
chmod 644 file.txt
chmod 600 file.txt
```

Symbolic Mode:

```bash
chmod u+x file.sh
chmod g-w file.txt
chmod o=r file.txt
```

Recursive Permission Change:

```bash
chmod -R 755 mydir
```

Key Learnings:

- chmod modifies file permissions.
- Numeric and symbolic methods can be used.
- Recursive permission changes can be applied using -R.

---

### 3. chown Command

Used to change file ownership.

Syntax:

```bash
chown owner file
chown owner:group file
```

Examples:

```bash
chown alice file.txt
chown alice:staff file.txt
```

Key Learnings:

- Changes file owner.
- Can modify owner and group together.

---

### 4. chgrp Command

Used to change group ownership.

Syntax:

```bash
chgrp group file
```

Example:

```bash
chgrp staff file.txt
```

Key Learnings:

- Changes file group ownership.
- Useful in shared environments.

---

### 5. Pipe ( | ) Concept

A pipe sends the output of one command as input to another command.

Syntax:

```bash
command1 | command2
```

Examples:

```bash
ls -1 *.txt | wc -l
ps aux | grep sshd
```

Common Usage:

```bash
cat file.txt | grep error
sort names.txt | uniq
history | tail -n 5
```

Key Learnings:

- Connects multiple commands.
- Avoids temporary files.
- Makes command execution efficient.
- Foundation of shell scripting.

---

### 6. tee Command

Reads from standard input and writes simultaneously to standard output and files.

Syntax:

```bash
tee [file]
```

Examples:

```bash
ls -l | tee output.txt
ls -l | tee -a output.txt
cat input.txt | tee output.txt
```

Key Learnings:

- Displays output and saves it at the same time.
- Useful for logging.
- Supports append mode using -a.

---

### 7. xargs Command

Builds and executes commands from standard input.

Syntax:

```bash
command | xargs command
```

Examples:

```bash
echo "1 2 3 4" | xargs
echo "1 2 3 4 5 6" | xargs -n 2
```

Using Replacement String:

```bash
xargs -I {}
```

Example:

```bash
ls file*.txt | xargs -I {} mv {} {}.bak
```

Key Learnings:

- Converts input into command arguments.
- Useful for batch processing.
- Reduces repetitive command execution.

---

### 8. Regular Expressions (Regex)

Regex is a pattern used to search, match and manipulate text.

Common Metacharacters:

| Symbol | Meaning |
|----------|----------|
| . | Any character |
| * | Zero or more |
| + | One or more |
| ? | Zero or one |
| ^ | Start of line |
| $ | End of line |
| [] | Character set |
| [^] | Negated set |
| \| | OR |
| () | Grouping |

Examples:

```bash
grep "^a" file.txt
grep "\.txt$" file.txt
grep "a.*e" file.txt
grep "[0-9]+" file.txt
```

Key Learnings:

- Regex simplifies pattern matching.
- Used heavily with grep, sed and awk.
- Helps in searching and filtering data.

---

### 9. grep, egrep and fgrep

#### grep

Global Regular Expression Print.

Syntax:

```bash
grep [options] "pattern" filename
```

Examples:

```bash
grep "error" logfile.txt
grep -ni "linux" file.txt
```

#### egrep

Extended grep.

Equivalent to:

```bash
grep -E
```

Examples:

```bash
egrep "cat|dog" file.txt
egrep -ni "Move|to" file.txt
```

#### fgrep

Fixed grep.

Equivalent to:

```bash
grep -F
```

Examples:

```bash
fgrep "cat" file.txt
fgrep "cat|dog" file.txt
```

Key Learnings:

- grep supports basic regular expressions.
- egrep supports extended regular expressions.
- fgrep treats patterns literally.

---

## Commands Practiced

```bash
grep -ni "Move" file.txt
egrep -ni "Move" file.txt
egrep -Eni "Move|to" file.txt

ls -l | tee file.txt
cat filee1.txt | grep "Delete" | tee filter.txt | wc -l

find . -name "file?.txt" -type f

echo "1 2 3 4 5 6" | xargs -n 2
echo "1 2 3 4 5 6" | xargs -n 4
echo "1 2 3 4 5 6" | xargs -n 8

ls file*.txt | xargs -I {} sh -c 'mv "$1" "${1%.txt}.bak"' _ {}
ls file*.bak | xargs -I {} sh -c 'mv "$1" "${1%.bak}.txt"' _ {}

echo -e "f1\nf2" | xargs -I {} mv {} {}.bak

egrep "cat|dog" new.txt
fgrep "cat|dog" new.txt

chmod 755 file.sh
chmod 644 file.txt
chmod 600 file.txt

chown owner file.txt
chgrp staff file.txt
```

---

## Hands-on Practice

### grep and egrep Practice

```bash
grep -ni "Move" file.txt
egrep -ni "Move" file.txt
egrep -Eni "Move|to" file.txt
```

Observed:

- Case-insensitive searching using -i.
- Displayed line numbers using -n.
- Used OR operator with egrep.

---

### tee Command Practice

```bash
ls -l | tee file.txt
cat filee1.txt | grep "Delete" | tee filter.txt | wc -l
```

Observed:

- Output displayed on screen and saved to file simultaneously.
- Combined tee with pipes.

---

### xargs Practice

```bash
echo "1 2 3 4 5 6" | xargs -n 2
echo "1 2 3 4 5 6" | xargs -n 4
echo "1 2 3 4 5 6" | xargs -n 8
```

Output:

```text
1 2
3 4
5 6
```

Learned grouping input arguments using -n.

---

### Batch Rename Using xargs

```bash
ls file*.txt | xargs -I {} sh -c 'mv "$1" "${1%.txt}.bak"' _ {}
ls file*.bak | xargs -I {} sh -c 'mv "$1" "${1%.bak}.txt"' _ {}
```

Observed:

- Renamed multiple files automatically.
- Restored original filenames.

---

### Regex Practice

Created:

```bash
cat > new.txt
```

Contents:

```text
cat
dog
cow
lion
tiger
```

Commands:

```bash
egrep "cat|dog" new.txt
fgrep "cat|dog" new.txt
```

Observed:

- egrep interpreted regex OR operator.
- fgrep treated pattern literally.

---

### Error Analysis

Commands producing errors:

```bash
grep -ni Move | backward file.txt
egrep cat|dog new.txt
echo "1 2 3" | xargs 4
```

Observed Errors:

- command not found
- invalid xargs usage
- incorrect pipe usage

Learned:

- Proper placement of pipes.
- Correct usage of xargs options.
- Difference between regex and fixed-string search.

---

## Comparison

| Command | Purpose |
|----------|----------|
| chmod | Change permissions |
| chown | Change owner |
| chgrp | Change group |
| pipe ( \| ) | Connect commands |
| tee | Display and save output |
| xargs | Convert input to command arguments |
| grep | Basic pattern search |
| egrep | Extended regex search |
| fgrep | Fixed string search |

---

## Key Takeaways

- Learned Linux file permission concepts.
- Practiced chmod, chown and chgrp commands.
- Understood numeric and symbolic permissions.
- Learned command chaining using pipes.
- Used tee for logging and output capture.
- Practiced xargs for batch processing.
- Learned Regular Expressions for pattern matching.
- Understood differences between grep, egrep and fgrep.
- Practiced troubleshooting common command-line errors.
