# Warp Drive Command Relationship Map

## Introduction

This Command Relationship Map provides an overview of how various shell and Warp commands relate to each other across different functional categories. The purpose of this map is to:

- Illustrate the hierarchical relationships between base commands and their variants
- Identify cross-functional dependencies between different command groups
- Provide an easy navigation system for finding related commands
- Help users understand how to build more complex commands from simpler ones
- Serve as a reference guide for command patterns and best practices

By understanding how commands relate to each other, users can more efficiently navigate the command library, discover logical extensions to their current workflows, and identify gaps or opportunities for new command definitions.

## Navigation

This map organises commands across four functional groups. Click on any of the links below to navigate to the detailed documentation for each group:

- [01-file-system-commands.md](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)
- [02-development-commands.md](file:///Users/ez/Local/appData/Warp/warp-drive-audit/02-development-commands.md)
- [03-workflow-commands.md](file:///Users/ez/Local/appData/Warp/warp-drive-audit/03-workflow-commands.md)
- [04-notes.md](file:///Users/ez/Local/appData/Warp/warp-drive-audit/04-notes.md)

## Command Relationship Maps

### Directory Navigation & Tree Structure

* **Base Directory Listing Commands**
  * `ls` - List directory contents
    * `ls -l` - Long format listing 
    * `ls -la` - Long format with hidden files
    * `ls -lah` - Human-readable sizes with hidden files
    * → Cross-reference: [Directory Analysis commands](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)
  
* **Directory Tree Visualisation**
  * `find . -type d` - List directories recursively
    * `find . -type d | sort` - Sorted directory listing
    * → Cross-reference: [Directory Analysis commands](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)
  * `tree` - Display directory tree structure
    * `tree -L [depth]` - Limit tree display to specified depth
    * `tree -a` - Include hidden files
    * `tree -d` - Show only directories
    * → Extension: [Run Directory Checker Python Script](file:///Users/ez/Local/appData/Warp/warp-drive-audit/02-development-commands.md)

* **Path Management**
  * `pwd` - Print working directory
  * `cd` - Change directory
    * `cd -` - Return to previous directory
    * `cd ~` - Navigate to home directory
  * `echo $PATH` - Display PATH environment variable
    * → Cross-reference: [Python Environment Path Management](file:///Users/ez/Local/appData/Warp/warp-drive-audit/02-development-commands.md)

* **specialised Path Discovery**
  * `find ~/Library/Mobile\ Documents/com~apple~CloudDocs/` - List iCloud Drive contents 
    * → Cross-reference: [Cloud Storage Path Management](03_Cloud_Storage_Management.md)
  * `find . -name "pattern"` - Find files/directories matching pattern
    * → Cross-reference: [Directory Analysis commands](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)

### Directory Analysis & Disk Usage

* **Disk Space Analysis**
  * `du` - Display disk usage
    * `du -h` - Human-readable sizes
    * `du -s` - Summary only
    * `du -sh` - Human-readable summary
    * `du -sh *` - Summarise disk usage for each item in current directory
    * `du -sh * | sort -h` - Sorted listing by size
    * → Cross-reference: [Directory Navigation commands](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)

* **File Search & Filtering**
  * `find` - Search for files in a directory hierarchy
    * `find . -type f` - Find all files
    * `find . -type d` - Find all directories
      * → Cross-reference: [Directory Navigation commands](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)
    * `find . -name "*.ext"` - Find by extension or pattern
    * `find . -size +10M` - Find by size
    * `find . -mtime -7` - Find by modification time
    * → Extension: [Python script integrations](file:///Users/ez/Local/appData/Warp/warp-drive-audit/02-development-commands.md)

* **File System Statistics**
  * `df -h` - Display file system disk space usage
  * `ls -la | wc -l` - Count files in directory
    * → Cross-reference: [Directory Navigation commands](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)
  * `find . -type f | wc -l` - Count files recursively

* **File Content Analysis**
  * `grep -r "pattern" .` - Search for pattern recursively
    * → Cross-reference: [Python Development searching](file:///Users/ez/Local/appData/Warp/warp-drive-audit/02-development-commands.md)
  * `wc -l file.txt` - Count lines in file

### Cloud Storage Management

* **iCloud Drive Commands**
  * `cd ~/Library/Mobile\ Documents/com~apple~CloudDocs/` - Navigate to iCloud Drive
    * → Cross-reference: [Directory Navigation commands](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)
  * `ls -la ~/Library/Mobile\ Documents/com~apple~CloudDocs/` - List iCloud contents
    * → Cross-reference: [Directory Analysis commands](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)
  * `find ~/Library/Mobile\ Documents/com~apple~CloudDocs/ -name "*.docx"` - Find documents
    * → Cross-reference: [Directory Analysis commands](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)

* **Cloud Environment Variables**
  * `echo $ICLOUD_DIR` - Display iCloud directory environment variable
  * `export ICLOUD_DIR=~/Library/Mobile\ Documents/com~apple~CloudDocs/` - Set iCloud environment variable
    * → Cross-reference: [Python environment variables](file:///Users/ez/Local/appData/Warp/warp-drive-audit/02-development-commands.md)

* **Cloud Synchronisation**
  * `rsync -av --progress source destination` - Sync files with progress
    * → Cross-reference: [Directory Analysis commands](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)
  * `cp -R source destination` - Copy files recursively
    * → Cross-reference: [Directory Navigation commands](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)

* **Dropbox Integration**
  * `cd ~/Dropbox` - Navigate to Dropbox folder
    * → Cross-reference: [Directory Navigation commands](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)
  * `ls -la ~/Dropbox` - List Dropbox contents
    * → Cross-reference: [Directory Analysis commands](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)

### Python Development Environment

* **Python Installation & Version**
  * `python --version` - Check Python version
  * `which python` - Locate Python executable
    * → Cross-reference: [Directory Navigation path discovery](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)
  * `python -m site` - Show Python site packages

* **Virtual Environment Management**
  * `python -m venv venv` - Create virtual environment
  * `source venv/bin/activate` - Activate virtual environment
    * → Cross-reference: [Directory Navigation commands](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)
  * `deactivate` - Deactivate virtual environment

* **Package Management**
  * `pip list` - List installed packages
  * `pip install package` - Install package
  * `pip freeze > requirements.txt` - Save dependencies
    * → Cross-reference: [Directory Analysis file creation](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)

* **Python Script Execution**
  * `python script.py` - Run Python script
  * `python -m module` - Run module as script
  * `chmod +x script.py && ./script.py` - Make script executable and run
    * → Cross-reference: [Directory Navigation commands](file:///Users/ez/Local/appData/Warp/warp-drive-audit/01-file-system-commands.md)

## Cross-Functional Command Patterns

### Directory & File Commands Across All Groups

1. **Navigation → Analysis → Action Pattern**:

	- Navigate to location (`cd`, `pwd`)
	- Analyse content (`ls`, `find`, `du`)
	- Take action (`cp`, `mv`, `python script.py`)

2. **Search → Filter → Process Pattern**:

	- Search for items (`find`, `grep`)
	- Filter results (`| grep`, `| sort`)
	- Process results (`| wc -l`, into Python script)
	
3. **Environment Setup → Execution Pattern**:

	- Setup environment (`export VAR=value`, `source venv/bin/activate`)
	- Execute commands within context (`python`, cloud commands)
	- Clean up (`deactivate`)

## Conclusion

This Command Relationship Map illustrates how commands across different functional groups relate to and build upon each other. By understanding these relationships, users can:

1. **Start Simple and Build Up**: Begin with base commands and gradually incorporate options and pipes to build more complex operations
2. **Leverage Cross-Functional Patterns**: Apply similar command patterns across different contexts
3. **Identify Command Families**: Recognise related commands that work together to achieve specific goals
4. **Discover New Workflows**: Find logical extensions to familiar commands and explore new functionality

### Extending This Map

This relationship map can be extended by:

1. Adding new commands to appropriate functional groups
2. Creating new cross-references as relationships are discovered
3. Developing additional functional groups for specialised workflows
4. Including examples that demonstrate combining commands across groups
5. Adding performance or best practice notes for complex command chains

When adding new commands, always consider where they fit in the existing hierarchy and what relationships they have with commands in other functional groups. Add appropriate cross-references to ensure users can navigate between related commands.

