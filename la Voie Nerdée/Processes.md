Whenever you execute a command or program in Linux, the operating system creates a *process* to run it.
A process is simply a running instance of a program.

The user account under whose permissions a program is running called a *process owner*.

> ⚠️ For security reasons, there is no way to change the owner of a currently running process in Linux

To manage process behavior, users can send [[signals]] to them.

## 🪪 PID/PPID

Each process identified by a unique number called a *Process ID (PID)*.

Key PID concepts:

- It helps the system track and manage processes
- No two running processes can have the same PID at the same time
- Once a process ends, its PID may be reused

Aside from PID, there is another attribute called a *Parent Process ID (PPID)*.
It identifies the PID of the process that spawned it.

A *parent process* is a process that creates one or more other processes (known as *child processes*) using the `fork()` system call.

If a parent process terminates before its child process, the child process becomes an *orphan*.
The `init` process adopts these orphans and becomes their new parent.

> ℹ️ Every process (except `init` and `kthreadd`) has its own PPID.

When a child process finishes execution, it becomes a *zombie* until its parent process performs a `wait()` operation to collect its [[Exit codes|termination status]].

## 🌀 Process flow

There are various [[system calls]] which control the process execution:

### fork()
- Create a new process by duplicating the calling process

### exec()
- Replace the current shell process with a new command process

### exit()
- Terminate the process
- Frees the memory that process was using
- Closes file descriptors

### wait()
- Suspend the execution of a process
- Retrieve the [[Exit codes|exit status]] of the last process it waited for

> [!example]- Flow scheme
![[Screenshot From 2026-01-29 22-06-41.png|400]]



[^1]: Sources:
	https://www.geeksforgeeks.org/linux-unix/processes-in-linuxunix/
	https://www.geeksforgeeks.org/linux-unix/kill-command-in-linux-with-examples/
