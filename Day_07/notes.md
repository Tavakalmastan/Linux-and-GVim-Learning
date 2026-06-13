# Day 07 - Environment Variables, PS1 Prompt Customization, grep, egrep, fgrep, pushd and popd

## Objective

Today's learning focused on Linux Environment Variables, Prompt Customization using PS1, File Searching using grep, egrep, and fgrep, and Directory Stack Management using pushd and popd commands.

---

## Topics Covered

### 1. Environment Variables

Environment variables store information used by the shell and applications.

Common Commands:

```bash
printenv
printenv HOME

echo $USER
echo $SHELL
echo $PWD
echo $HOSTNAME
```

Setting Variables:

```bash
export MY_VARIABLE="value"
export PATH="$PATH:/usr/local/bin"
```

Common Environment Variables:

| Variable | Description                 |
| -------- | --------------------------- |
| USER     | Current username            |
| HOME     | Home directory              |
| PWD      | Present working directory   |
| PATH     | Search path for executables |
| SHELL    | Current shell               |
| HOSTNAME | System hostname             |

### Key Learnings

* Viewed system environment variables using `printenv`.
* Accessed variables using `echo $VARIABLE`.
* Created custom environment variables using `export`.
* Understood the role of PATH and shell variables.

---

### 2. PS1 Prompt Customization

PS1 defines the appearance of the terminal prompt.

Basic Syntax:

```bash
PS1="your prompt string"
```

Common Escape Sequences:

| Sequence | Meaning                     |
| -------- | --------------------------- |
| \u       | Username                    |
| \h       | Hostname                    |
| \w       | Current directory           |
| \W       | Current directory name only |
| \d       | Date                        |
| \t       | Time (24-hour format)       |
| @        | Time (12-hour format)       |
| $        | User prompt symbol          |

Examples:

```bash
PS1="\u@\h:\w\$ "
```

```bash
PS1="\t \w\$ "
```

Making PS1 Permanent:

```bash
gvim ~/.bashrc
source ~/.bashrc
```

### Key Learnings

* Customized terminal prompts.
* Displayed username, hostname, directory, date, and time.
* Applied ANSI color codes to prompts.
* Learned how to save prompt settings permanently.

---

### 3. grep Command

grep (Global Regular Expression Print) is used to search text patterns in files.

Syntax:

```bash
grep [options] pattern filename
```

Common Options:

```bash
grep -i pattern file
grep -n pattern file
grep -c pattern file
grep -v pattern file
grep -r pattern directory
grep -w pattern file
grep -A 2 pattern file
grep -B 2 pattern file
grep -C 2 pattern file
```

Examples:

```bash
grep "error" logfile.txt
grep -i "warning" logfile.txt
grep -n "root" passwd.txt
grep -c "failed" auth.log
grep -v "#" file.txt
```

### Key Learnings

* Search for matching patterns.
* Ignore case sensitivity.
* Count matching lines.
* Display line numbers.
* Search recursively.
* Match whole words only.

---

### 4. egrep Command

egrep is used for extended regular expression matching.

Examples:

```bash
egrep "error|warning|critical" logfile.txt
egrep "[0-9]+" file.txt
```

### Key Learnings

* Supports extended regular expressions.
* Search multiple patterns using `|`.
* Equivalent to `grep -E`.

---

### 5. fgrep Command

fgrep is used to search fixed strings without interpreting regular expressions.

Examples:

```bash
fgrep "Linux" file.txt
fgrep "Hello World" notes.txt
```

### Key Learnings

* Searches exact text strings.
* Does not treat special characters as regular expressions.
* Faster for simple string matching.
* Equivalent to `grep -F`.

---

### 6. pushd and popd Commands

Used to manage directory navigation using a directory stack.

#### pushd

Pushes current directory onto the stack and moves to another directory.

```bash
pushd /var/log
```

#### popd

Returns to the previous directory.

```bash
popd
```

#### dirs

Displays the current directory stack.

```bash
dirs
dirs -v
dirs -c
```

### Key Learnings

* Stored directories in a stack.
* Quickly switched between multiple directories.
* Returned to previous directories using `popd`.
* Viewed and managed the directory stack.

---

## Commands Practiced

### Environment Variables

```bash
echo $USER
echo $SHELL
echo $PWD
echo $HOSTNAME

printenv

export Linux="/cygdrive/E/GVIM_Practice/pd/PD_training/linux"
echo $Linux
```

### Directory Stack Commands

```bash
pushd /cygdrive
pushd E
pushd GVIM_Practice
pushd pd
pushd PD_training
pushd linux
```

### PS1 Prompt Customization

```bash
PS1="\u@\h:\w\n\$"
```

```bash
export PS1="\[\e[1;36m\][\u@\h]\[\e[0m\] \[\e[1;33m\]\w\[\e[0m\]\n\$ "
```

### grep Practice

```bash
grep "error" file.txt
grep -i "error" file.txt
grep -n "error" file.txt
grep -c "error" file.txt
grep -v "error" file.txt
```

### egrep Practice

```bash
egrep "error|warning" logfile.txt
egrep "[0-9]+" file.txt
```

### fgrep Practice

```bash
fgrep "Linux" file.txt
fgrep "error" logfile.txt
```

---

## Error Handling Practice

```bash
pusgd pd
```

Output:

```text
-bash: pusgd: command not found
```

### Observations

* Linux commands are case-sensitive.
* Incorrect command names generate "command not found" errors.
* Variable names are case-sensitive.

---

## Practical Learning Outcomes

* Explored Linux environment variables.
* Created and exported custom variables.
* Customized terminal prompts using PS1.
* Practiced ANSI color formatting.
* Learned text filtering using grep, egrep, and fgrep.
* Performed pattern matching with regular expressions.
* Used pushd, popd, and dirs for efficient directory navigation.
* Improved troubleshooting skills through command experimentation.
