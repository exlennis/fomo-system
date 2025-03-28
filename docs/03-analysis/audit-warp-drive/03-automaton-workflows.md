# Workflow Commands

This file contains commands that automate processes or enhance productivity in your daily workflow. These commands help streamline repetitive tasks, manage system processes, and improve overall efficiency when working with the command line.

## Kill the process running on a port

### Syntax
```bash
lsof -t -i:[port] | xargs kill
```

### Description
This command identifies and terminates any process that is currently using a specified network port. It's particularly useful when you need to free up a port that's being used by a process that you want to stop, such as when you're encountering "address already in use" errors during development.

The command works in two parts:
1. `lsof -t -i:[port]` finds the process ID (PID) of the process using the specified port
2. `xargs kill` takes that PID and sends a termination signal to it

### Example Usage
```bash
# Kill any process running on port 3000
lsof -t -i:3000 | xargs kill

# Kill any process running on port 8080
lsof -t -i:8080 | xargs kill
```

## Process Monitoring Commands

### ps - Process Status

#### Syntax
```bash
ps [options]
```

#### Description
The `ps` command displays process status, providing information about active processes. There are many options available to customize the output.

#### Example Usage
```bash
# Show all processes, including those belonging to other users
ps aux

# Show a long listing, including the process state
ps -l

# Show information for a specific process ID
ps -p <PID>

# Filter processes by name
ps aux | grep [process_name]
```

### top - Real-time Process Viewer

#### Syntax
```bash
top
```

#### Description
The `top` command provides a real-time, dynamic view of running processes, similar to Activity Monitor but in the terminal. It displays a continuously updating list of processes, sorted by CPU usage by default.

#### Example Usage
```bash
# Launch top
top

# While in top:
# - Press 'o' to filter by process name
# - Press 'q' to quit
# - Press 'k' to kill a process (you'll be prompted for the PID)
```

### jobs - View Background Jobs

#### Syntax
```bash
jobs
```

#### Description
The `jobs` command shows processes that were started in the current terminal session and put in the background. This is useful for managing multiple tasks within the same terminal window.

#### Example Usage
```bash
# List all background jobs in the current terminal session
jobs

# Resume a suspended job in the foreground
fg %[job_number]

# Resume a suspended job in the background
bg %[job_number]
```

### Resume a Suspended Process

#### Syntax
```bash
fg [%job_number]
```
or
```bash
kill -CONT <PID>
```

#### Description
These commands allow you to resume a process that has been suspended (typically by pressing Ctrl+Z).

#### Example Usage
```bash
# Resume the most recently suspended job
fg

# Resume job #2
fg %2

# Resume a process with a specific PID
kill -CONT 12345
```

