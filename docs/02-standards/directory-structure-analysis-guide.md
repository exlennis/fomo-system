# Directory Examination and Analysis Guide

*About this document:*
- **Purpose**: Guide users through a systematic approach to examine directories and optimise their structure
- **Primary focus**: Analytical commands for understanding directory content and structure
- **Contains**: Terminal commands and procedures for examining directory structure
- **Key components**: Command usage, options, examples, best practices for directory analysis


## Purpose
Understanding directory structure is crucial for maintaining an organised and efficient system. This **systematic approach** provides a complete picture of the directory in question, helping make informed decisions about **naming conventions** and **structural organisation**.

The **commands** below are designed to be used in sequence to examine directory contents effectively, providing insights into file sizes, types, hierarchies, and relationships, enabling informed suggestions about **file management**.

## Essential Commands

### 1. Listing Directory Contents (ls):
Examine the current directory with details

```bash
ls -lah
```

**Options Explained**
- `-l`: Long format, showing detailed information
- `-a`: Show all files (including hidden ones)
- `-h`: Human-readable sizes (KB, MB, GB)

**Example Output**
```plain
total 128K
drwxr-xr-x   4 user  staff   128B 10 Jan 14:30 .
drwxr-xr-x   8 user  staff   256B 10 Jan 14:20 ..
-rw-r--r--   1 user  staff    12K 10 Jan 14:25 document.pdf
drwxr-xr-x   2 user  staff    64B 10 Jan 14:28 images/
```

**Output Information**
- File permissions (rwx)
- Number of links
- Owner and group
- File size
- Last modified date
- File/directory name

### 2. Directory Tree Structure (tree)
For a tree-like view of the directory structure (up to 2 levels deep):

```bash
tree -L 2
```

**Options Explained**
- `-L n`: Limit depth to n levels
- `-d`: Show only directories
- `-h`: Show file sizes
- `-a`: Show all files including hidden ones

#### Alternative (without tree)
```bash
find . -maxdepth 2 -type d -print | sed -e 's;[^/]*/;|____;g;s;____|; |;g'
```

### 3. Disk Usage Analysis (du)
To get disk usage information for each subfolder:

```bash
du -hd 1 | sort -hr
```

**Options Explained**
- `-h`: Human-readable sizes
- `-d 1`: Only one level deep
- `sort -hr`: Sort by size (human-readable) in reverse order

**Example Output**
```bash
1.2G    ./Videos
650M    ./Documents
128M    ./Images
24K     ./Config
2.0G    .
```

### 4. Find Command for File Searching
To search for specific types of files or patterns:

```bash
find . -type f -name "*.extension"
```

#### Useful Find Options
- `-type f`: Find files
- `-type d`: Find directories
- `-name "pattern"`: Search by name
- `-size +10M`: Files larger than 10MB
- `-mtime -7`: Modified in last 7 days

#### File Type Distribution
```bash
find . -type f | sed 's/.*\.//' | sort | uniq -c | sort -nr
```

## Best Practices and Tips

1. **Performance Optimisation**
- Use appropriate depth limits with tree and find commands
- Add `-prune` to `find` commands to skip specific directories
- Monitor command performance in large directories

2. **Organisation Tips**
- Start with `ls -lah` for an initial overview
- Use `du -hd 1` to identify space-heavy directories
- Combine `find` with `grep` for targeted searches
- Create a systematic examination routine

3. **Safety Tips**
- Always use `-type f` with `find` when targeting files
- Test complex find commands with `-print` first
- Use quotes around patterns to prevent unwanted expansion

4. **Productivity Tips**
- Create aliases in your `.zshrc` or `.bash_profile`:
    ```bash
    alias dsize='du -hd 1 | sort -hr'
    alias ll='ls -lah'
    ```
- Use tab completion to navigate directories
- Leverage command history (up arrow) for frequent commands

## Recommended Workflow

1. Start with `ls -lah` to get a detailed view of the current directory
2. Use `tree -L 2` to visualise the directory structure
3. Run `du -hd 1 | sort -hr` to identify large directories
4. Use `find` commands to locate specific file types or patterns
5. Document your findings to inform reorganisation decisions

This systematic approach ensures you understand:
- File and directory permissions
- Space utilisation
- Directory hierarchy
- File type distribution
- Modified dates and timestamps

These insights enable informed decisions about:
- Directory restructuring
- File grouping strategies
- Naming conventions
- Space optimisation
- Access permissions
