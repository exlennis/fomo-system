# Development Commands

This document contains commands related to programming environments, Git, and development tools. These commands are essential for software developers to manage their development environments and workflows. All documentation follows Australian English spelling conventions.

## Python Environment Commands

### Python Environment Check

#### Syntax
```bash
ls -la ~/.pyenv/versions
find ~/[path] -name "venv" -o -name ".venv" -type d
```

#### Description
These commands are used to check and locate Python virtual environments on your system. They help identify where Python installations are stored, both in pyenv and as standalone virtual environments.

#### Example Usage
```bash
# Check for pyenv installations
ls -la ~/.pyenv/versions 2>/dev/null || echo "No pyenv versions found"

# Find virtualenv directories in projects
find ~/local/-PROJECTS-Dev -name "venv" -o -name ".venv" -type d 2>/dev/null
```

## Conda Environment Commands

### Conda Environment Check

#### Syntax
```bash
ls -la ~/anaconda3/envs
ls -la ~/.conda/envs
```

#### Description
These commands help locate and list Conda environments installed on your system, both in the standard Anaconda directory and in the user's home directory.

#### Example Usage
```bash
# Check for Anaconda environments
ls -la ~/anaconda3/envs 2>/dev/null || echo "No Anaconda environments found"

# Check for user Conda environments
ls -la ~/.conda/envs 2>/dev/null || echo "No user Conda environments found"
```

## File Tagging (macOS)

### tag Command

#### Syntax
```bash
tag [options] [file(s)]
```

#### Description
The `tag` command is a macOS utility that allows you to manage Finder tags from the command line. It enables you to add, remove, set, and search for tags on files and directories, helping with file organisation and search.

#### Example Usage

##### Listing Tag Usage Statistics
```bash
tag --usage '*'  # List all tags with file counts
tag --usage tagname  # Count files with specific tag
```

##### Listing Tags on a File
```bash
tag -l filename
```

##### Finding Files with Specific Tags
```bash
tag -f tagname
```

##### Adding Tags to a File
```bash
tag -a tagname filename
```

##### Removing Tags from a File
```bash
tag -r tagname filename
```

##### Setting Tags (replacing all existing tags)
```bash
tag -s "tag1,tag2" filename
```

#### Common Options
- `--home`: Limit search to user home directory
- `--local`: Include local filesystems
- `--network`: Include network filesystems
- `-t`: Display tags
- `-g`: Garrulous output (multi-line tags)
- `-R`: For recursive operations
- `-c`: For coloured output

#### Installation
The `tag` command can be installed via Homebrew:

```bash
brew install tag
```

