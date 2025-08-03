# 0x03-shell_variables_expansions

## Task 0: `<o>`

**Script Name:** `0-alias`

**Description:**
This script creates a shell alias that redefines the `ls` command to execute `rm *` instead. When the script is sourced, any call to `ls` will delete all files in the current directory.

**Usage:**
```bash
source ./0-alias
ls  # This will now run `rm *` instead of listing files
