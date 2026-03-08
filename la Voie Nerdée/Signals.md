In Linux, process *signals* are software interrupts used for inter-process communication and managing [[processes|process]] behavior.

When a signal is sent to a process, the operating system interrupts its execution and notifies it of some system event, such as termination, pause, etc.

If a process has defined a custom method to handle a specific signal, that method is executed; otherwise the system uses the default signal handler.

## Usage

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
