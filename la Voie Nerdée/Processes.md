Whenever you execute a command or program in Linux, the operating system creates a *process* to run it.
A process is simply a running instance of a program.

Each command in Linux creates only one process, but an application on the other hand can initiate multiple processes to fulfill different tasks.

The user account under whose permissions a program is running called a *process owner*.

> ⚠️ For security reasons, here is no way to change the owner of a currently running process in Linux

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

When a child process finishes execution, it becomes a *zombie* until its parent process performs a `wait()` operation to collect its termination status.

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

![[Screenshot From 2026-01-29 22-06-41.png|400]]

## 📡 Signals

Users can send *signals* to processes to communicate with them directly.

When a signal is sent to a process, the operating system interrupts its execution and notifies it of some system event, such as termination, pause, etc.

If a process has defined a custom method to handle a specific signal, that method is executed; otherwise the system uses the default signal handler.

To send a specific signal to process, use `kill` command:

```bash
kill [-signal] <PID>
# Sends SIGTERM signal by default
```

Signal can be specified by its number or a signal name (either with or without the `SIG` prefix).

### Common signals

| *Signal name* | *Number* | *Description*                                                        |
| ------------- | -------- | -------------------------------------------------------------------- |
| `SIGHUP`      | `1`      | Notify a process that its controlling terminal has been disconnected |
| `SIGINT`      | `2`      | Request a graceful termination of a process initiated *by user*      |
| `SIGKILL`     | `9`      | Terminate a process immediately without cleanup                      |
| `SIGTERM`     | `15`     | Request a graceful termination of a process                          |
| `SIGCONT`     | `18`     | Resume the execution of a process                                    |
| `SIGSTOP`     | `19`     | Pause a process execution                                            |






[^1]: Sources:
	https://www.geeksforgeeks.org/linux-unix/processes-in-linuxunix/
	https://www.geeksforgeeks.org/linux-unix/kill-command-in-linux-with-examples/
