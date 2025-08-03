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
