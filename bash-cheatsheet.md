# Basic Terminal Commands Cheat Sheet

These are the most common terminal commands you'll use.

## Show Current Folder

Prints the path of the directory you are currently in.

```bash
pwd
```

Example output:

```text
C:\Users\Larissa\Projects\my-repo
```

> pwd stands for "print working directory"
---

## Change Folder

Move into another directory.

```bash
cd <folder-name>
```

To move up one level:

```bash
cd ..
```
> cd is the abbreviation for "change directory" 

---

## List Files and Folders

Shows the contents of the current directory.

```bash
ls
```

> ls is short for "list"

When you want to see also hidden files and folders in your directory, use the -a flag (stands for "all"):

```bash
ls -a 
```

---

## Create a New Folder

Creates a new directory.

```bash
mkdir <folder-name>
```

> mkdir stands for "make directory"
---

## Remove a File

Deletes a file.

```bash
rm <file-name>
```

Example:

```bash
rm draft.txt
```

> Be careful: deleted files in the terminal cannot easily be recovered! 

> rm stands for "remove"


---

## Senta Tests

She is writing Code.

```bash
rm <doodle>
```

Example:

```bash
rm woop.txt
```

> This is a different comment


---

## Copy a File

Creates a copy of a file.

```bash
cp <source-file> <new-file>
```

Example:

```bash
cp notes.md notes_backup.md
```

> cp stands for "copy"
---

## Quick Overview

| Command | Purpose |
|----------|----------|
| `pwd` | Show current folder |
| `cd` | Change folder |
| `ls` | List files and folders |
| `mkdir` | Create a folder |
| `rm` | Remove a file |
| `cp` | Copy a file |

These six commands are enough to navigate most Git repositories and work comfortably with AI coding assistants such as Claude Code, Codex, and other terminal-based tools.
