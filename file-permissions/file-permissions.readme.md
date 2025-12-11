Here is a **clean, perfectly structured, beautifully formatted** README-ready version of your content.
This formatting matches **professional GitHub documentation style** + uses **clear headings, tables, code blocks, spacing, and consistency**.

Just copy-paste into your **README.md** — it's already in Markdown.

---

# **File Management in Linux**

##  File & Directory Management

| Command                  | Description                                         |
| ------------------------ | --------------------------------------------------- |
| `ls`                     | Lists files and directories in the current location |
| `cd /path/to/dir`        | Changes the working directory                       |
| `pwd`                    | Prints the current working directory                |
| `mkdir new_folder`       | Creates a new directory                             |
| `rmdir empty_folder`     | Removes an empty directory                          |
| `rm file.txt`            | Deletes a file                                      |
| `rm -r folder`           | Deletes a folder and its contents                   |
| `cp file1.txt file2.txt` | Copies a file                                       |
| `cp -r dir1 dir2`        | Copies a directory recursively                      |
| `mv old new`             | Moves or renames a file/directory                   |

---

##  File Viewing & Editing

| Command                    | Description                       |
| -------------------------- | --------------------------------- |
| `cat file.txt`             | Displays file content             |
| `less file.txt`            | View file with scroll support     |
| `head -n 10 file.txt`      | Shows first 10 lines              |
| `tail -n 10 file.txt`      | Shows last 10 lines               |
| `nano file.txt`            | Opens file in Nano editor         |
| `vim file.txt`             | Opens file in Vim editor          |
| `echo "Hello" > file.txt`  | Writes text to a file (overwrite) |
| `echo "Hello" >> file.txt` | Appends text to a file            |

---

##  Modes in Vim Editor

| Mode             | Description                                                   |
| ---------------- | ------------------------------------------------------------- |
| **Normal Mode**  | Navigation and commands *(default mode)*                      |
| **Insert Mode**  | Used for editing text <br> → Press `i`, exit with `Esc`       |
| **Command Mode** | Saving, quitting, searching <br> → Press `:` from Normal mode |

### Common Vim Save/Quit Commands

| Command | Meaning             |
| ------- | ------------------- |
| `:w`    | Save file           |
| `:wq`   | Save and exit       |
| `:q!`   | Quit without saving |

---

#  **Introduction to File Permissions**

Linux uses 3 permission levels:

* **Owner (User)** → file creator
* **Group** → assigned group users
* **Others** → everyone else

### Permission Types

| Symbol | Value | Meaning |
| ------ | ----- | ------- |
| `r`    | 4     | Read    |
| `w`    | 2     | Write   |
| `x`    | 1     | Execute |

### Check permissions:

```bash
ls -l filename
```

Example output:

```
-rwxr--r-- 1 user group 1234 Mar 28 10:00 myfile.sh
```

---

#  **Changing File Permissions with `chmod`**

##  Using Symbolic Mode

Examples:

```bash
chmod u+x filename      # Add execute for user
chmod g-w filename      # Remove write for group
chmod o=r filename      # Read-only for others
chmod u=rwx,g=rx,o= filename   # Set custom permissions
```

---

## Using Octal (Numeric) Mode

| Number | Meaning |
| ------ | ------- |
| 4      | Read    |
| 2      | Write   |
| 1      | Execute |

Examples:

```bash
chmod 755 filename   # rwx r-x r-x
chmod 644 filename   # rw- r-- r--
chmod 700 filename   # rwx --- ---
```

---

# **Changing Ownership with `chown`**

```bash
chown newuser filename      # Change file owner
```

---

Just tell me!
