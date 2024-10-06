# Lab 5 - Command Line Interface (CLI) Essentials

## 1. I/O Redirection

### Standard Output Redirection
- **Default behavior**: Command output is displayed on the terminal.
- **Redirection**: Use `>` to redirect the output to a file. Example:
    ```bash
    ls > output.txt
    ```
    This saves the output of the `ls` command into the `output.txt` file (overwrites if it exists).
- **Appending output**: Use `>>` to append the output to a file:
    ```bash
    ls >> output.txt
    ```
    This adds the output of `ls` to `output.txt` without overwriting it.

### Standard Input Redirection
- **Default behavior**: Commands take input from the keyboard.
- **Redirection**: Use `<` to redirect input from a file:
    ```bash
    sort < input.txt
    ```
    This sorts the content of `input.txt`.

- **Mixing input and output redirection**:
    ```bash
    sort < input.txt > sorted_output.txt
    ```
    This reads the content from `input.txt`, sorts it, and saves the result in `sorted_output.txt`.

---

## 2. Pipelines (`|`)
- **Purpose**: Pipes (`|`) link commands, making the output of one command the input for another.
    ```bash
    command1 | command2 | command3
    ```
    Example:
    ```bash
    ls | grep "search_term"
    ```
    This command lists the directory contents and searches for files or directories containing the "search_term".

---

## 3. File Permissions and User Management

### File Permissions
- **Types**: `r` (read), `w` (write), `x` (execute)
- **Categories**: Owner, group, others
- **Example**: `rw-r--r--` means:
    - **Owner**: Read and write (`rw-`)
    - **Group**: Read-only (`r--`)
    - **Others**: Read-only (`r--`)

### Changing Permissions
- **Use `chmod`** to modify permissions:
    ```bash
    chmod 644 file.txt
    ```

### Superuser Access (`sudo`)
- **Purpose**: A superuser can execute administrative commands.
    ```bash
    sudo [command]
    ```

---

## 4. Text Processing Commands

### `grep` (Global Regular Expression Print)
- **Purpose**: Search for patterns in files.
    ```bash
    grep "search_term" file.txt
    ```
    Example: Find all instances of "error" in `log.txt`:
    ```bash
    grep -i "error" log.txt
    ```
    Common options:
    - `-i`: Case-insensitive search.
    - `-v`: Inverts the search, showing lines that do **not** match the search term.
    - `-n`: Displays line numbers with matches.
    - `-r`: Recursive search.

---

## 5. File Downloading Tools

### `wget`
- **Usage**: Downloads files from the internet:
    ```bash
    wget [URL]
    ```

### `curl`
- **Usage**: Transfers data from or to a server:
    ```bash
    curl -O [URL]
    ```

---

## 6. Shell Scripting Basics
- **Create a script** using a text editor (e.g., `nano`, `vim`):
    ```bash
    nano script.sh
    ```
- **Make it executable**:
    ```bash
    chmod +x script.sh
    ```
- **Run the script**:
    ```bash
    ./script.sh
    ```

---

## 7. Additional Commands

### `history`
- **Shows the list of previously executed commands**:
    ```bash
    history
    ```
- **Save history to a file**:
    ```bash
    history > commands.txt
    ```

---

## Submission Instructions
- Ensure personalized notes are prepared for submission.
- Refer to Cybercampus for detailed instructions.
