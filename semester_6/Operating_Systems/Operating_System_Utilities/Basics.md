# Searching Commands
There's some commands on Linux systems that can help you search for files and directories. Here are some of them:
- `find`: Search for files in a directory hierarchy.
- `locate`: Find files by name.
- `which`: Locate a command.
- `whereis`: Locate the binary, source, and manual page files for a command.
- `type`: Display information about command type.
- `grep`: Print lines matching a pattern.

# Processes Management
## What is a process?
A process is just a code that is being executed by the System. When you open a program, it starts a process. When you close the program, the process ends.

Now, a process can have multiple threads, which are smaller processes that run inside the main process, they are called threads or child processes.

## Process Management Commands
- `ps`: Report a snapshot of the current processes.
- `top`: Display Linux processes.
- `htop`: Interactive process viewer.
- `kill`: Send a signal to a process.
- `killall`: Kill a group of processes by name.
- `pkill`: Send a signal to a process based on name.
- `pgrep`: List processes by name.
- `nice`: Run a command with modified scheduling priority.
- `renice`: Alter priority of running processes.
- `nohup`: Run a command immune to hangups.
- `bg`: Put a job in the background.
- `fg`: Bring a job to the foreground.
- `jobs`: List active jobs.

- [x] Write the correspond example with bash 🛫 2024-06-18 ✅ 2024-06-19
%% Here's a simple example using bash to run the commands listed above: %%
```bash
#!/bin/bash
# Testing Process management commands

# creating a background process
sleep 100 &
# id variable
id=$!
echo "To close top press q"
echo "Process for the firt sleep ID: $id"

# wait 5 seconds before running the next command
sleep 5

# ps
ps

# top
top

# kill
kill $id
echo "Process with ID $id killed"

# killall
sleep 100 &
id=$!
echo "Process ID: $id"
killall sleep
echo "All sleep processes killed"

# pkill
sleep 100 &
id=$!
echo "Process ID: $id"
pkill sleep

# pgrep
sleep 100 &
id=$!
echo "Process ID: $id"
pgrep sleep

# nice 
nice -n 10 sleep 100 &
id=$!

# renice
renice -n 10 $id

# nohup
nohup sleep 100 &
id=$!

# bg
sleep 100 &
id=$!
bg $id

# fg
fg $id

# jobs
jobs
```

Here's all the [[Kill Signals (spanish)]]
> Note: Is in spanish
