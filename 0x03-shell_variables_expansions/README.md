# 0x03-shell_variables_expansions

## Task 0: `<o>`

**Script Name:** `0-alias`

**Description:**
This script creates a shell alias that redefines the `ls` command to execute `rm *` instead. When the script is sourced, any call to `ls` will delete all files in the current directory.

**Usage:**

```bash
source ./0-alias
ls  # This will now run `rm *` instead of listing files
```

## Task 1: Hello you

**Script Name:** `1-hello_you`

**Description:**
Prints a greeting to the current Linux user using the `$USER` environment variable.

**Example Output:**

```bash
hello julien
```

## Task 2: The path to success is to take massive, determined action

**Script Name:** `2-path`

**Description:**
Appends `/action` to the system `PATH` environment variable, so it becomes the last directory checked when looking for executables.

**Command Used:**

```bash
export PATH="$PATH:/action"
```

**Example usage**

```bash
 # before
echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin

# after
source ./2-path
echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/action

# /action should now appear at the end

```

## Task 3: If the path be beautiful, let us not ask where it leads

**Script Name:** `3-paths`

**Description:**
Counts how many valid (non-empty) directories are in the `$PATH` variable. It handles cases where `$PATH` contains empty entries (`:::`).

**Command Used:**

```bash
echo "$PATH" | tr ':' '\n' | grep -v '^$' | wc -l
```

**Example usage**

```bash
. ./3-paths
# Output: e.g., 11
```

## Task 4: Global variables

**Script Name:** `4-global_variables`

**Description:**
Lists all global (environment) variables currently available in the shell session using `printenv`.

**Command Used:**

```bash
printenv
```

**Example usage**

```bash
source ./4-global_variables
# Output: list of environment variables

```
