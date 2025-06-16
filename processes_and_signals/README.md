Here's a comprehensive README file for your Shell, processes and signals project:

# Shell, Processes and Signals

This project is part of the ALU curriculum focusing on understanding Linux processes, signals, and process management using Bash scripting.

## Project Overview

**Author:** Sylvain Kalache  
**Weight:** 1  
**Project Duration:** May 26, 2025 12:00 AM - Jun 20, 2025 11:59 PM

## Learning Objectives

By the end of this project, you should be able to explain the following concepts without external help:

### General Concepts
- What is a PID (Process ID)
- What is a process
- How to find a process' PID
- How to kill a process
- What is a signal
- What are the 2 signals that cannot be ignored

## Resources

### Reading Materials
- [Linux PID]()
- [Linux process]()
- [Linux signal]()

### Command References
Use `man` or `help` for these commands:
- `ps` - Display running processes
- `pgrep` - Find process IDs by name
- `pkill` - Kill processes by name
- `kill` - Terminate processes by PID
- `exit` - Exit the shell
- `trap` - Handle signals in scripts

## Requirements

### General Requirements
- **Allowed editors:** `vi`, `vim`, `emacs`
- **OS:** Ubuntu 20.04 LTS
- All files must end with a new line
- All Bash scripts must be executable
- Scripts must pass `Shellcheck` (version 0.7.0) without errors
- First line of all Bash scripts: `#!/usr/bin/env bash`
- Second line must be a comment explaining the script's purpose

## Project Structure


alu-shell/
├── processes_and_signals/
│   ├── README.md
│   ├── 0-what-is-my-pid
│   ├── 1-list_your_processes
│   ├── 2-show_your_bash_pid
│   ├── 3-show_your_bash_pid_made_easy
│   ├── 4-to_infinity_and_beyond
│   ├── 5-dont_stop_me_now
│   ├── 6-stop_me_if_you_can
│   ├── 7-highlander
│   ├── 8-beheaded_process
│   ├── 9-process_and_pid_file
│   ├── 10-process_and_pid_file
│   ├── 11-manage_my_process
│   └── manage_my_process


## Tasks Overview

| Task | Script Name | Description |
|------|-------------|-------------|
| 0 | `0-what-is-my-pid` | Display the script's own PID |
| 1 | `1-list_your_processes` | List all running processes |
| 2 | `2-show_your_bash_pid` | Show Bash process PID using ps and grep |
| 3 | `3-show_your_bash_pid_made_easy` | Show Bash PID using pgrep |
| 4 | `4-to_infinity_and_beyond` | Infinite loop displaying message |
| 5 | `5-dont_stop_me_now` | Kill the infinity script using kill |
| 6 | `6-stop_me_if_you_can` | Kill the infinity script using pkill |
| 7 | `7-highlander` | Script that handles SIGTERM signal |
| 8 | `8-beheaded_process` | Kill the highlander script |
| 9 | `9-process_and_pid_file` | Advanced process with PID file and signal handling |
| 10 | `10-process_and_pid_file` | Complex signal handling script |
| 11 | `11-manage_my_process` | Init script for process management |

## Usage Examples

### Running Scripts

bash
# Make script executable
chmod +x script_name
Run script
./script_name


### Testing Process Management

bash
# Start a background process
./4-to_infinity_and_beyond &
Kill it from another terminal
./5-dont_stop_me_now


## Key Concepts

### Process ID (PID)
- Unique identifier for each running process
- Accessible via `$$` variable in current process
- Can be found using `ps`, `pgrep`, or reading `/proc/` directory

### Signals
- SIGTERM (15): Termination request (can be caught)
- SIGKILL (9): Force kill (cannot be caught)
- SIGINT (2): Interrupt (Ctrl+C)
- SIGQUIT (3): Quit signal

### Signal Handling

bash
# Trap signal in script
trap 'echo "Signal received"' SIGTERM

## Repository Information

- **GitHub Repository:** `alu-shell`
- **Directory:** `processes_and_signals`
- **Files:** All task scripts and this README

## Author

**Alieu O. Jobe**  
ALU Student - Introduction to Linux and IT Tools

## Additional Resources

For comprehensive signal information, refer to the signal handling documentation and man pages for each command used in this project.

This README provides a complete overview of your project, including all the essential information about the tasks, requirements, and concepts covered in the Shell, processes and signals project.
