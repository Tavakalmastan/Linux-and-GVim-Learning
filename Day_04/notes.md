# Day 04 - File Viewing and Content Management Commands

## Objective

Today's learning focused on Linux commands used to view, read, navigate, and inspect file contents efficiently.

---

## Topics Covered

### 1. cat Command

Used to display, create, and combine files.

Common usage:

```bash
cat file.txt
cat file1.txt file2.txt
cat > newfile.txt
```

Useful options:

```bash
cat -n file.txt
cat -b file.txt
cat -s file.txt
cat -E file.txt
```

Key Learnings:

- Display file contents.
- Create files from terminal.
- Combine multiple files.
- Show line numbers.

---

### 2. less Command

Used to view large files page by page.

Basic usage:

```bash
less file.txt
```

Navigation:

```text
Space  -> Next page
b      -> Previous page
g      -> First line
G      -> Last line
/pattern -> Search forward
n      -> Next match
q      -> Quit
```

Key Learnings:

- Efficient for large files.
- Supports forward and backward navigation.
- Search functionality available.

---

### 3. more Command

Used to read file contents one screen at a time.

Basic usage:

```bash
more file.txt
```

Navigation:

```text
Space -> Next page
Enter -> Next line
q     -> Quit
```

Key Learnings:

- Simple file viewer.
- Mainly forward navigation.
- Useful for quick inspection.

---

### 4. head Command

Used to display the beginning of a file.

Examples:

```bash
head file.txt
head -n 5 file.txt
head -c 20 file.txt
```

Key Learnings:

- Shows first 10 lines by default.
- Can display a specific number of lines.
- Useful for checking file headers.

---

### 5. tail Command

Used to display the end of a file.

Examples:

```bash
tail file.txt
tail -n 5 file.txt
tail -f logfile.txt
```

Key Learnings:

- Shows last 10 lines by default.
- Useful for log monitoring.
- Real-time monitoring using `tail -f`.

---

## Commands Practiced

```bash
cat file.txt
cat -n file.txt
less file.txt
more file.txt
head file.txt
head -n 5 file.txt
tail file.txt
tail -n 5 file.txt
tail -f logfile.txt
```

---

## Comparison

| Command | Purpose |
|----------|----------|
| cat | Display or create files |
| less | View large files interactively |
| more | View files page by page |
| head | View beginning of file |
| tail | View end of file |

---

## Key Takeaways

- Learned different methods to read file contents.
- Understood when to use cat, less, and more.
- Practiced viewing the first and last portions of files.
- Learned basic navigation while viewing large files.
