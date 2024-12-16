# Shell Script Failure with Large Files

This repository demonstrates a common issue in shell scripting: handling extremely large files.  The script `bug.sh` attempts to process a large file line by line. However, it can fail if the file exceeds system limits on open files or available memory.

The solution, `bugSolution.sh`, addresses this by processing the file in smaller chunks, reducing the resource burden on the system.

## Bug Description
The original script reads the entire file into memory at once, leading to potential failure with very large files.

## Solution
The improved script processes the file in chunks using `head` and `tail` commands.