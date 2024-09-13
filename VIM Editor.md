
---

# VI Editor / VIM Editor

The **VI editor** is one of the most popular and classic text editors in the Linux family. It is widely used by Linux users for creating scripts, editing configuration files, and handling general text editing tasks.

---

## Why Use VI Editor?
1. **Available in Almost All Linux Distributions**: Pre-installed in nearly every Linux distribution.
2. **Consistency Across Platforms**: The same editing experience across different platforms and Linux distributions.
3. **Powerful Yet Lightweight**: Offers advanced features while being fast and efficient.
4. **Highly Customizable**: Vim, an extended version of VI, supports plugins and configuration for extensive customization.
5. **Widely Loved**: Millions of Linux users prefer VI and Vim for their speed, flexibility, and powerful command set.

---

## Modes in VI/VIM Editor
VI operates in two primary modes:

1. **Command Mode**: For navigation, deletion, copying, pasting, and more.
2. **Insert Mode**: Used for text input and editing.

### Switching Between Modes
- **Insert Mode**: Press `i` or `a` in command mode to switch to insert mode.
- **Command Mode**: Press `ESC` to return to command mode from insert mode.

---

## Basic VI/VIM Commands

### Opening and Closing Files
- **Open a file for editing**:  
  ```bash
  vi filename.txt
  ```
  Example:  
  ```bash
  vi abc.txt
  ```

- **Save and Exit**:  
  - Press `ESC` to enter command mode, then type `:wq` and press `Enter`.
  - To quit without saving, use `:q!`.

---

## VI Command Mode Shortcuts

| Command             | Description                                                |
|---------------------|------------------------------------------------------------|
| `i`                 | Insert text before the cursor.                             |
| `a`                 | Insert text after the cursor.                              |
| `o`                 | Open a new line below the cursor and go into insert mode.   |
| `ESC`               | Exit insert mode and return to command mode.               |
| `:w`                | Save the file.                                             |
| `:q`                | Quit VI (only if no changes have been made).               |
| `:wq`               | Save and exit VI.                                          |
| `:q!`               | Quit without saving changes.                               |
| `dd`                | Delete the current line.                                   |
| `[n]dd`             | Delete `n` lines starting from the current line.           |
| `yy`                | Copy (yank) the current line.                              |
| `p`                 | Paste the copied line after the cursor.                    |
| `/pattern`          | Search for a pattern in the file.                          |
| `n`                 | Repeat the last search.                                    |
| `u`                 | Undo the last action.                                      |
| `Ctrl+r`            | Redo the undone action.                                    |
| `G`                 | Go to the last line of the file.                           |
| `gg`                | Go to the first line of the file.                          |
| `h`, `j`, `k`, `l`  | Move left, down, up, and right (Arrow keys alternative).   |

---

## Cursor Movement and Navigation

| Command   | Description                                |
|-----------|--------------------------------------------|
| `k`       | Move cursor up                             |
| `j`       | Move cursor down                           |
| `h`       | Move cursor left                           |
| `l`       | Move cursor right                          |
| `gg`      | Jump to the first line of the file         |
| `G`       | Jump to the last line of the file          |
| `:n`      | Jump to line `n`                           |
| `Ctrl+f`  | Move forward one screen                    |
| `Ctrl+b`  | Move backward one screen                   |

---

## Searching Within Files

- **Search**:  
  ```bash
  /pattern
  ```
  Example:  
  ```bash
  /error
  ```
  - **Description**: Searches for the word "error" within the file. Press `n` to find the next occurrence.

- **Search and Replace**:  
  ```bash
  :s/[old_word]/[new_word]/g
  ```
  Example:  
  ```bash
  :s/error/success/g
  ```
  - **Description**: Replaces all occurrences of `error` with `success` in the current line. Use `:%s/old/new/g` to replace across the entire file.

---

## File Operations

| Command   | Description                                |
|-----------|--------------------------------------------|
| `:w`      | Save the file.                             |
| `:q`      | Quit the editor.                           |
| `:wq`     | Save and quit.                             |
| `:q!`     | Quit without saving.                       |
| `:x`      | Save and quit (same as `:wq`).             |

---

## Line Numbering

- **Enable Line Numbers**:  
  ```bash
  :set nu
  ```
- **Disable Line Numbers**:  
  ```bash
  :set nonu
  ```

---