# Day 09 - Text Processing Commands, AWK, SED, Alias and Shell Scripting

## Objective

Today's learning focused on advanced Linux text processing tools, stream editing, pattern scanning, command aliases, useful system commands, bash configuration files, and introductory shell scripting.

---

## Topics Covered

### 1. sed Command

sed (Stream Editor) is used to process and modify text streams.

Basic Syntax:

```bash
sed [options] 'command' file.txt
```

Common Commands:

```bash
sed 's/old/new/' file.txt
sed 's/old/new/g' file.txt
sed '/pattern/d' file.txt
sed -n '/pattern/p' file.txt
sed '3i\Inserted Text' file.txt
sed '2a\Appended Text' file.txt
sed '2c\Modified Text' file.txt
```

Key Learnings:

- Replace text in files.
- Delete lines matching patterns.
- Insert and append text.
- Print selected lines.
- Perform in-place editing using `-i`.

---

### 2. AWK Command

AWK is a powerful text processing and pattern scanning tool.

Basic Syntax:

```bash
awk 'pattern { action }' file.txt
```

Built-in Variables:

| Variable | Meaning |
|----------|----------|
| $0 | Entire line |
| $1,$2,... | Fields |
| NF | Number of fields |
| NR | Record number |
| FS | Field separator |
| OFS | Output field separator |

Examples:

```bash
awk '{print}' file.txt
awk '{print $1}' file.txt
awk '{print $1,$3}' file.txt
awk 'END{print NR}' file.txt
awk '{sum+=$4} END{print sum}' file.txt
```

Key Learnings:

- Extract specific columns.
- Perform calculations.
- Filter records using conditions.
- Generate summaries and reports.

---

### 3. alias Command

Alias creates shortcuts for frequently used commands.

Examples:

```bash
alias ll='ls -lh'
alias la='ls -A'
alias gs='git status'
```

Remove Alias:

```bash
unalias ll
```

Make Alias Permanent:

```bash
echo "alias ll='ls -lh'" >> ~/.bashrc
source ~/.bashrc
```

Key Learnings:

- Simplifies long commands.
- Improves productivity.
- Can be stored in `.bashrc`.

---

### 4. Essential Linux Commands

#### id

Displays user and group information.

```bash
id
```

#### hostname

Displays system hostname.

```bash
hostname
```

#### whoami

Displays current username.

```bash
whoami
```

#### who

Displays logged-in users.

```bash
who
```

#### date

Displays current date and time.

```bash
date
```

#### cal

Displays calendar.

```bash
cal
```

#### ps

Displays running processes.

```bash
ps -ef
```

#### kill

Terminates a process.

```bash
kill PID
```

#### ping

Checks network connectivity.

```bash
ping google.com
```

Key Learnings:

- Monitor system information.
- Check active users.
- View and manage processes.
- Verify network connectivity.

---

### 5. .bashrc File

`.bashrc` is executed whenever a new interactive bash shell starts.

Common Uses:

```bash
alias ll='ls -lh'

export EDITOR=vim

export PATH="$HOME/.local/bin:$PATH"

export PS1="\u@\h:\w\$ "
```

Key Learnings:

- Store aliases.
- Define environment variables.
- Customize shell prompt.
- Configure shell behavior.

---

### 6. tr Command

Used to translate or transform characters.

Examples:

```bash
echo "linux" | tr 'a-z' 'A-Z'

echo "Linux Commands" | tr ' ' '_'

echo "abc123" | tr -d '0-9'

echo "Linux    command" | tr -s ' '
```

Key Learnings:

- Convert uppercase and lowercase.
- Replace characters.
- Delete characters.
- Squeeze repeated characters.

---

### 7. cut Command

Used to extract specific columns or character positions.

Examples:

```bash
cut -d " " -f1 file.txt

cut -d " " -f1,3 file.txt

cut -d " " -f1,4 file.txt

cut -c 1-5 file.txt

cut -c 1-8 file.txt
```

Key Learnings:

- Extract fields from structured text.
- Select multiple columns.
- Extract fixed character ranges.

---

### 8. Introduction to Shell Scripting

Shell scripting automates repetitive Linux tasks.

Basic Structure:

```bash
#!/usr/bin/bash/

echo "Hello World"
```

File Permission:

```bash
chmod 755 script.sh
```

Execute Script:

```bash
./script.sh
```

Key Learnings:

- Automate command execution.
- Create reusable scripts.
- Improve productivity.

---

### 9. Conditional Statements in Shell Scripting

Syntax:

```bash
if [ condition ]; then
    commands
else
    commands
fi
```

Example:

```bash
#!/usr/bin/bash/

file="practice.txt"

if [ -f "$file" ]; then
    echo "File Exists"
else
    echo "File not found"
fi
```

Key Learnings:

- Use conditions to control execution flow.
- Check file existence.
- Understand if-else-fi structure.

---

### 10. Arithmetic Operations in Shell Script

Example:

```bash
#!/usr/bin/bash/

echo "Enter First Number"
read a

echo "Enter Second Number"
read b

echo "Sum = $((a+b))"
echo "Diff = $((a-b))"
echo "Product = $((a*b))"
```

Key Learnings:

- Read user input.
- Perform arithmetic operations.
- Display computed results.

---

## Commands Practiced

### AWK Commands

```bash
awk '{print $2}' sample.txt
awk '{print $NF}' sample.txt
awk '{print $2,$NF}' sample.txt
awk '$3=="IT"{print}' sample.txt
awk '$3=="HR"{print}' sample.txt
awk '$4>30000{print}' sample.txt
awk '$4>=40000{print}' sample.txt
awk '{sum+=$4} END{print sum}' sample.txt
awk '{sum+=$4} END{print sum/NR}' sample.txt
awk 'END{print NR}' sample.txt
awk 'BEGIN{max=0}{if($4>max)max=$4}END{print max}' sample.txt
awk '{print NR,$0}' sample.txt
awk '{print $1,$3}' sample.txt
```

### sed Commands

```bash
sed -n '1p' practice.txt
sed -n '5p' practice.txt
sed -n '/print/p' practice.txt
sed -n '/salary/p' practice.txt
sed -n '2,+4p' practice.txt
sed -n '2,+5p' practice.txt
sed -n '1~2p' practice.txt
sed '1d' practice.txt
sed '$d' practice.txt
sed '4 c Hello world' practice.txt
```

### tr Commands

```bash
echo "linux" | tr 'a-z' 'A-Z'
echo "linux" | tr 'A-Z' 'a-z'
echo "Linux Commands" | tr ' ' '_'
echo "abc123" | tr -d '0-9'
echo "abc123" | tr -d 'a-z'
echo "Linux    command" | tr -s ' '
```

### cut Commands

```bash
cut -d " " -f1 cut.txt
cut -d " " -f1,3 cut.txt
cut -d " " -f1,4 cut.txt
cut -c 1-5 cut.txt
cut -c 1-8 cut.txt
```

### Shell Scripting Commands

```bash
chmod 755 file.sh
chmod 777 file.sh
./file.sh

chmod 777 file1.sh
./file1.sh
```

---

## Practical Learning Outcomes

- Practiced text manipulation using sed.
- Processed structured data using awk.
- Created command shortcuts using alias.
- Learned useful Linux administration commands.
- Customized shell environment using .bashrc.
- Performed character translation using tr.
- Extracted fields and character ranges using cut.
- Wrote and executed basic shell scripts.
- Implemented file existence checks using if-else conditions.
- Performed arithmetic operations in shell scripts.
- Improved debugging skills by analyzing command and script errors.

