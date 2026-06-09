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

---

## Additional Practice

### Commands Practiced

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls
dir2  dir3

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ cat > file1.txt
Day 01
Insert Mode
Normal Mode
Navigation Commands
Search and Replace
Copy and Paste
Split Windows
Folding
Save and Exit Commands
Day 02
Visual Mode
Visual Line Mode
Visual Block Mode
Text Selection Techniques
Vimrc Configuration
GVim Customization
Line Numbers and Editor Options
Search Highlighting
Auto Indentation
Tab Management
Creating and Closing Tabs
Switching Between Tabs
Macros (Recording Mode)
Macro Execution and Reuse
Multi Cursor Editing
Advanced Editing Features
Day 03
Bash Shell
Linux Command Syntax
pwd Command
ls Command
Linux File Types
cd Command
touch Command
mkdir Command
rm and rmdir Commands
cp Command
mv Command
Input/Output Redirection


Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ cat  file1.txt
Day 01
Insert Mode
Normal Mode
Navigation Commands
Search and Replace
Copy and Paste
Split Windows
Folding
Save and Exit Commands
Day 02
Visual Mode
Visual Line Mode
Visual Block Mode
Text Selection Techniques
Vimrc Configuration
GVim Customization
Line Numbers and Editor Options
Search Highlighting
Auto Indentation
Tab Management
Creating and Closing Tabs
Switching Between Tabs
Macros (Recording Mode)
Macro Execution and Reuse
Multi Cursor Editing
Advanced Editing Features
Day 03
Bash Shell
Linux Command Syntax
pwd Command
ls Command
Linux File Types
cd Command
touch Command
mkdir Command
rm and rmdir Commands
cp Command
mv Command
Input/Output Redirection

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ less 4 file1.txt
4: No such file or directory
Press RETURN to continue

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ less file.txt
file.txt: No such file or directory

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls
dir2  dir3  file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ less file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ less file1.txt 5

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ less 2 file1.txt
2: No such file or directory
Press RETURN to continue

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ head 5 file1.txt
head: cannot open '5' for reading: No such file or directory
==> file1.txt <==
Day 01
Insert Mode
Normal Mode
Navigation Commands
Search and Replace
Copy and Paste
Split Windows
Folding
Save and Exit Commands
Day 02

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ head 2 file1.txt
head: cannot open '2' for reading: No such file or directory
==> file1.txt <==
Day 01
Insert Mode
Normal Mode
Navigation Commands
Search and Replace
Copy and Paste
Split Windows
Folding
Save and Exit Commands
Day 02

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ head file1.txt 1
==> file1.txt <==
Day 01
Insert Mode
Normal Mode
Navigation Commands
Search and Replace
Copy and Paste
Split Windows
Folding
Save and Exit Commands
Day 02
head: cannot open '1' for reading: No such file or directory

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ head file1.txt -5
head: invalid trailing option -- 5
Try 'head --help' for more information.

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ head file1.txt -n 4
Day 01
Insert Mode
Normal Mode
Navigation Commands

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ head -n 6 file1.txt
Day 01
Insert Mode
Normal Mode
Navigation Commands
Search and Replace
Copy and Paste

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ tail -n 3 file1.txt
cp Command
mv Command
Input/Output Redirection

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ grep -ni "Day" file1.txt
1:Day 01
10:Day 02
27:Day 03

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ find . -name *.txt -type f
./file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ touch file[2-5].txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls
 dir2   dir3   file1.txt  'file[2-5].txt'

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ rm file\[2-5\].txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls
dir2  dir3  file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ rm file{2-5}.txt
rm: cannot remove 'file{2-5}.txt': No such file or directory

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ touch file{2-5}.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls
dir2  dir3  file1.txt  file{2-5}.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ rm file\{2-5\}.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls
dir2  dir3  file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ find . -name * -type d
find: paths must precede expression: `dir3'
find: possible unquoted pattern after predicate `-name'?

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ find . -name "*" -type d
.
./dir2
./dir3

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ chmod
chmod: missing operand
Try 'chmod --help' for more information.

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -l
total 1
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:40 dir2
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:36 dir3
-rwxrw----+ 1 Tavakalmastan Tavakalmastan 666 Jun  9 18:42 file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ chmod 000 dir2

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -l
total 1
drwx------+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:40 dir2
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:36 dir3
-rwxrw----+ 1 Tavakalmastan Tavakalmastan 666 Jun  9 18:42 file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ chmod 111 dir2

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -l
total 1
drwx--x--x+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:40 dir2
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:36 dir3
-rwxrw----+ 1 Tavakalmastan Tavakalmastan 666 Jun  9 18:42 file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ chmod o+rw dir2

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -l
total 1
drwx--xrwx+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:40 dir2
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:36 dir3
-rwxrw----+ 1 Tavakalmastan Tavakalmastan 666 Jun  9 18:42 file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ chmod g+rw dir2

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -l
total 1
drwxrwxrwx+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:40 dir2
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:36 dir3
-rwxrw----+ 1 Tavakalmastan Tavakalmastan 666 Jun  9 18:42 file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ chmod o-rw dir2

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -l
total 1
drwxrwx--x+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:40 dir2
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:36 dir3
-rwxrw----+ 1 Tavakalmastan Tavakalmastan 666 Jun  9 18:42 file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ chmod o-rwx dir2

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -l
total 1
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:40 dir2
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:36 dir3
-rwxrw----+ 1 Tavakalmastan Tavakalmastan 666 Jun  9 18:42 file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -l
total 1
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:40 dir2
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:36 dir3
-rwxrw----+ 1 Tavakalmastan Tavakalmastan 666 Jun  9 18:42 file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -L
dir2  dir3  file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -d
.

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -s
total 1
0 dir2  0 dir3  1 file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -p
dir2/  dir3/  file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -c
dir2  file1.txt  dir3

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -a
.  ..  dir2  dir3  file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -la
total 9
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:48 .
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:36 ..
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:40 dir2
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:36 dir3
-rwxrw----+ 1 Tavakalmastan Tavakalmastan 666 Jun  9 18:42 file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -l
total 1
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:40 dir2
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:36 dir3
-rwxrw----+ 1 Tavakalmastan Tavakalmastan 666 Jun  9 18:42 file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -R
.:
dir2  dir3  file1.txt

./dir2:

./dir3:

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls
dir2  dir3  file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -h
dir2  dir3  file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -t
file1.txt  dir2  dir3

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -s
total 1
0 dir2  0 dir3  1 file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls -l
total 1
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:40 dir2
drwxrwx---+ 1 Tavakalmastan Tavakalmastan   0 Jun  9 18:36 dir3
-rwxrw----+ 1 Tavakalmastan Tavakalmastan 666 Jun  9 18:42 file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ l
-bash: l: command not found

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ echo "Hello world" > output.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ cat output.txt
Hello world

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ echo "hello">f1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ echo "linux" >f2.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ echo "hello">f2.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ cat f2.txt
hello

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls
dir2  dir3  f1.txt  f2.txt  file1.txt  output.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ rm -i output.txt
rm: remove regular file 'output.txt'? n

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls
dir2  dir3  f1.txt  f2.txt  file1.txt  output.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ dir2 -p
-bash: dir2: command not found

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ man -p
man: option requires an argument -- 'p'
Try 'man --help' or 'man --usage' for more information.

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ man argu
No manual entry for argu

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ man
What manual page do you want?
For example, try 'man man'.

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ man man

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ man --pager
man: option '--pager' requires an argument
Try 'man --help' or 'man --usage' for more information.

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ man pager
No manual entry for pager

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls
dir2  dir3  f1.txt  f2.txt  file1.txt  output.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ cd dir2

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice/dir2
$ ls

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice/dir2
$ cd ..

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ mv output.txt dir2

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls
dir2  dir3  f1.txt  f2.txt  file1.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ cd dir2

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice/dir2
$ ls
output.txt

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice/dir2
$ cd ..

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ cp -v file.txt dir2
cp: cannot stat 'file.txt': No such file or directory

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ cp -v file1.txt dir2
'file1.txt' -> 'dir2/file1.txt'

Tavakalmastan@Mastan /cygdrive/E/GVIM_practice/pd/PD_training/linux/practice
$ ls
dir2  dir3  f1.txt  f2.txt  file1.txt


