# Vim Modes, Movement & Editing Tutorial

This tutorial covers Vim’s core modes, how to move around, select text, and perform common edits using Vim’s modal interface.

---

## 1. Vim’s Core Modes

| Mode             | How to Enter                    | Purpose                                           |
| ---------------- | ------------------------------- | ------------------------------------------------- |
| **Normal**       | `<Esc>` (or on start)           | Navigate, delete, copy, paste, run commands (`:`) |
| **Insert**       | `i`, `I`, `a`, `A`, `o`, `O`    | Insert text                                       |
| **Visual**       | `v` (char), `V` (line), `<C-v>` | Select text                                       |
| **Command-line** | `:`                             | Save/quit/search/other ex-commands                |

> **Tip:** Look for “– INSERT –” in the status line to know you’re in Insert mode.

---

## 2. Switching Modes

- **Normal → Insert**

  - `i` Insert **before** cursor
  - `I` Insert at **start** of line
  - `a` Append **after** cursor
  - `A` Append at **end** of line
  - `o` Open **new line** below
  - `O` Open **new line** above

- **Insert → Normal**

  - `<Esc>`

- **Normal → Visual**

  - `v` Character‑wise select
  - `V` Line‑wise select
  - `<C-v>` Block‑wise select

- **Visual → Normal**

  - `<Esc>`

- **Normal → Command-line**
  - `:` then command (e.g. `:w`, `:q!`, `:e filename`)

---

## 3. Basic Cursor Movement (`h`, `j`, `k`, `l`)

In **Normal** and **Visual** modes, use:

| Key | Direction | Description                     |
| --- | --------- | ------------------------------- |
| `h` | Left      | Move cursor one character left  |
| `j` | Down      | Move cursor one line down       |
| `k` | Up        | Move cursor one line up         |
| `l` | Right     | Move cursor one character right |

---

## 4. Advanced Motions & Line Navigation

| Command | Action                                        |
| ------- | --------------------------------------------- |
| `w`     | Jump forward to **start** of next word        |
| `b`     | Jump backward to **start** of previous word   |
| `e`     | Jump to **end** of current/next word          |
| `0`     | Go to **first** character of the current line |
| `^`     | Go to **first** non-blank character of line   |
| `$`     | Go to **last** character of the current line  |
| `gg`    | Go to **first** line of the file              |
| `G`     | Go to **last** line of the file               |

---

## 5. Editing Commands

| Command  | Action                                |
| -------- | ------------------------------------- |
| `dd`     | Delete **entire** current line        |
| `yy`     | Yank (copy) **entire** current line   |
| `p`      | Paste **after** the cursor/selection  |
| `P`      | Paste **before** the cursor/selection |
| `u`      | Undo last change                      |
| `Ctrl‑r` | Redo (undo the undo)                  |

> **Tip:** Prepend a number to repeat: `3dd` deletes three lines, `2yy` yanks two lines, `5j` moves down five lines.

---

## 6. Visual Mode Selection & Operations

1. **Enter Visual mode**:
   - `v` (character)
   - `V` (line)
   - `<C-v>` (block)
2. **Extend selection** using moves (`h`/`j`/`k`/`l`, `w`, `b`, etc.).
3. **Operate on selection**:
   - `d` Delete
   - `y` Yank (copy)
   - `>` Indent right
   - `<` Indent left
4. **Exit Visual mode**:
   - `<Esc>`

---

## 7. Quick Practice

1. Open a file:
   ```bash
   vim example.txt
   ```
