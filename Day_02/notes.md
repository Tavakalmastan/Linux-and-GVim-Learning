# Day 02 - Visual Mode, Vimrc, Tabs and Macros

## Objective

Learn advanced text selection techniques, GVim customization using .vimrc, tab management, and automation using macros.

---

# Visual Mode

Visual mode allows selecting text for copying, deleting, changing, and formatting.

## Commands

| Command | Description |
|----------|------------|
| v | Visual mode (character selection) |
| V | Visual line mode |
| Ctrl + v | Visual block mode |

---

# Visual Block Mode

Visual Block Mode allows editing multiple lines simultaneously.

## Common Commands

| Command | Description |
|----------|------------|
| Ctrl + v | Enter block mode |
| I | Insert at beginning of selected block |
| A | Append at end of selected block |
| C | Change selected block |
| y | Copy selected block |
| d | Delete selected block |

---

## Example

Before:

apple
banana
grapes

After selecting a column using Ctrl+v:

I#

Result:

#apple
#banana
#grapes

---

# Vim Configuration (.vimrc)

The .vimrc file stores user settings and customizations.

Open vimrc:

```vim
:sp ~/.vimrc
```

---

## Common Vimrc Settings

```vim
set number
set hlsearch
set incsearch
set autoindent
set tabstop=4
set syntax=on
set showmode
set nocompatible
set backspace=indent,eol,start
```

### Purpose

- Display line numbers
- Highlight search results
- Incremental search
- Auto indentation
- Syntax highlighting
- Better editing experience

---

# GVim Options

## Line Numbers

```vim
:set number
```

Disable:

```vim
:set nonumber
```

---

## Word Wrap

Enable:

```vim
:set wrap
```

Disable:

```vim
:set nowrap
```

---

## Tab Settings

```vim
:set tabstop=4
:set expandtab
:set noexpandtab
```

---

## Search Settings

```vim
:set ignorecase
:set hlsearch
:set incsearch
```

---

# Tabs

Tabs allow working with multiple files.

## Create New Tab

```vim
:tabnew
```

or

```vim
:tabe filename
```

---

## Navigation

```vim
:tabnext
:tabprevious
:tabfirst
:tablast
```

---

## Close Tab

```vim
:tabclose
```

---

# Macros (Recording Mode)

Macros automate repetitive tasks.

---

## Start Recording

```vim
qa
```

Record actions into register a.

---

## Stop Recording

```vim
q
```

---

## Execute Macro

```vim
@a
```

---

## Repeat Last Macro

```vim
@@
```

---

## Example

Task:

Add semicolon to multiple lines.

1. Start recording

```vim
qa
```

2. Perform editing

3. Stop recording

```vim
q
```

4. Replay

```vim
@a
```

---

# Additional Advanced Features Learned

## Multi Cursor Editing

Edit multiple lines efficiently using Visual Block Mode.

---

## Split Windows

```vim
:split
:vsplit
```

---

## Syntax Highlighting

```vim
syntax on
```

Provides colorized source code.

---

## Code Folding

Hide unnecessary sections.

```vim
zf
```

---

# Practice Performed

- Used Visual Mode
- Used Visual Block Mode
- Configured .vimrc
- Enabled line numbers
- Practiced tab management
- Created and executed macros
- Explored GVim customization options

---

# Key Takeaways

- Visual Block Mode is powerful for column editing.
- Vimrc helps customize the editor permanently.
- Tabs improve multi-file management.
- Macros automate repetitive tasks.
- GVim becomes significantly more productive through customization.

---
