# File System Commands

This document contains commands related to file system navigation, manipulation, and directory listings. The commands are documented with their syntax, description, and example usage. All descriptions follow Australian English spelling conventions.

## tree

### Command Name
tree

### Syntax
```bash
tree [options] [directory]
```

Common options:
```
-L level       Limit the level of directory depth
-d             Show only directories
--dirsfirst    List directories before files
--noreport     Turn off file/directory count at end of tree listing
```

### Description
The `tree` command displays the directory structure in a hierarchical, tree-like format. It visualises the directory structure with indentation and connecting lines, making it easier to understand the organisation of files and folders on your system.

### Example Usage
```bash
# List directory structure with depth of 2, showing only directories
tree -L 2 -d --dirsfirst --noreport /Users/ez

# List directory structure with depth of 3, showing only directories
tree -L 3 -d --dirsfirst --noreport /Users/ez/Library/CloudStorage

# Example of directory listing across multiple locations
echo -e "\n=== Home Directory ===";
tree -L 2 -d --dirsfirst --noreport /Users/ez 2>/dev/null;

echo -e "\n=== Projects ===";
tree -L 2 -d --dirsfirst --noreport /Users/ez/Library/CloudStorage/Dropbox-Personal/-PROJECTS- 2>/dev/null;
```

## find

### Command Name
find

### Syntax
```bash
find [path...] [expression]
```

Common options:
```
-type [f|d]     Specify file type: f (regular file) or d (directory)
-name pattern   Search for files/directories matching the pattern
-o              Logical OR operator to combine multiple search patterns
-maxdepth n     Descend at most n directory levels
-not            Negate the next expression
-size n         File uses n units of space (c: bytes, k: kilobytes, M: megabytes, G: gigabytes)
```

### Description
The `find` command searches for files or directories in a directory hierarchy based on specified criteria such as name patterns, file types, or other file attributes. It's a powerful tool for locating files in a file system and can be combined with other commands for further processing of the found files.

### Example Usage
```bash
# Find all files with .txt extension in the current directory
find . -type f -name "*.txt"

# Find all directories containing "mono" (case-insensitive) in their name
find "/directory-path/Fonts/Foundries/" -type d -name "*[Mm]ono*" | sort

# Find files with multiple name patterns (logical OR)
find "/directory-path/Fonts/Foundries/" -type f -name "*[Mm]ono*" -o -name "*[Mm]onospace*" -o -name "*[Ff]ixed*" -o -name "*[Cc]onsole*" -o -name "*[Tt]ypewriter*" | sort

# Find files modified in the last 24 hours
find /home/user -type f -mtime -1

# Find empty files
find . -type f -empty

# Find and execute commands on found files (delete all .tmp files)
find . -type f -name "*.tmp" -exec rm {} \;
```


