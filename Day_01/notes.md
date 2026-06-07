# Day 01 - Introduction to GVim

## Objective

Learn the basics of GVim, understand different modes, navigation commands, text editing, search/replace operations, screen splitting, and file handling.

---

## What is GVim?

GVim (Graphical Vim) is an advanced text editor based on the Vim editor.

### Applications
- Programming
- Scripting
- Configuration file editing
- General text editing
- Efficient keyboard-based workflow

---

# Modes in GVim

## 1. Insert Mode

Used for entering and editing text.

### Commands

| Command | Description |
|----------|------------|
| i | Insert before cursor |
| I | Insert at beginning of line |
| a | Append after cursor |
| A | Append at end of line |
| o | Open new line below |
| O | Open new line above |

### Exit Insert Mode

```
Esc
```

---

## 2. Normal (Escape) Mode

Used for navigation and editing.

### Navigation Commands

| Command | Description |
|----------|------------|
| h | Move left |
| j | Move down |
| k | Move up |
| l | Move right |
| w | Move to next word |
| b | Move to previous word |
| 0 | Move to beginning of line |
| $ | Move to end of line |
| gg | Move to first line |
| G | Move to last line |

---

## Editing Commands

| Command | Description |
|----------|------------|
| x | Delete character |
| dd | Delete current line |
| D | Delete to end of line |
| u | Undo |
| Ctrl + r | Redo |

---

## Search Commands

| Command | Description |
|----------|------------|
| /word | Search forward |
| ?word | Search backward |
| n | Next occurrence |
| N | Previous occurrence |

---

## Save and Exit Commands

| Command | Description |
|----------|------------|
| :w | Save file |
| :q | Quit |
| :q! | Quit without saving |
| :wq | Save and quit |
| :x | Save and quit if modified |
| :w filename | Save with different filename |

---

## Search and Replace

Replace a word globally:

```vim
:%s/old_word/new_word/g
```

Example:

```vim
:%s/welcome/training/g
```

---

## Copy and Paste

### Copy Line

```vim
yy
```

### Paste

```vim
p
```

### Multiple Paste

```vim
5p
```

Pastes copied content 5 times.

---

## Screen Splitting

### Vertical Split

```vim
:vsplit
```

### Horizontal Split

```vim
:split
```

---

## Folding

Hide selected lines:

```vim
zf
```

---

## Page Navigation

| Command | Description |
|----------|------------|
| Ctrl + f | Forward one page |
| Ctrl + b | Backward one page |
| H | Top of current page |
| M | Middle of current page |
| L | Bottom of current page |

---

## Documentation

Open help documentation:

```vim
:help
```

Example:

```vim
:help.txt
```

---

# Practice Performed

- Learned Insert Mode commands
- Learned Normal Mode navigation
- Practiced saving and quitting files
- Used search and replace
- Practiced copy and paste operations
- Learned screen splitting
- Learned folding commands
- Practiced page navigation

---

# Key Takeaways

- GVim is highly keyboard-driven.
- Normal Mode is the default working mode.
- Insert Mode is used only when text entry is required.
- Navigation becomes much faster using shortcuts.
- Search/Replace significantly improves editing efficiency.
