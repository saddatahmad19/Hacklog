# Hacklog

**Hacklog** is a lightweight, scross-shell session logger fro devs working in directory based projects.

## Features

- Logs all commands to the log file located in given project root directory
- Ignore common utilities commands; configurable to your own desires
- Timestamped notes
- Interactive or inline note entry
- View logs wia command or pipe into `less`

## Installation
1. Clone this project into your directory of choice
`git clone https://github.com/saddatahmad19/Hacklog.git`

- Move the script to the location you store all your scripts

2. Make the script exectable in the directory you stored the script in
`chmod +x hacklog`

3. Add the script path to your shell
**Bash**
`export PATH="$HOME/path/for/script:$PATH"`

**Zsh**
```
if [[ -d "$HOME/Scripts" ]]; then
	export PATH="$HOME/Scripts:$PATH"
fi
```

## Commands And Usage

1. Start logger
- Go to the projects main directory
`source hacklog init`
This will generate a .hacklog file in the current directory, and will store commands ran in any deeper directory, or subdirectories.
**Arguments**     
`--file=`: Custom log file path
`--ignore=`: Space seperated list of commands to exclude from logging

Begin commanding and all will be stored!

2. Add Note to the Log
Add a timestamped note to the logger, to explain why you ran `whoami` 15 times while thinking of what to do. 
`hacklog note "Add note here"
or
`hacklog note` and begin writing; exit with Ctrl+D

3. View Logs
View logs for current project
`hacklog view`

4. Stop logger
Once you are done with your informational etching endevours, stop the logger.
`source hacklog stop`

## Tested System
Currently, this works on my Kali Linux machine, please feel free to test it out and let me know if it works on your system.

### Operating System

**Tested On**:
- Kali Linux

### Shell

- Bash
- Zsh

### Dependencies

- Standard POSIX Utilities
    - date
    - less
    - sed

