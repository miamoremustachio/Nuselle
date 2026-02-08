The *nice value (niceness)* in Linux is a mechanism used to control the CPU scheduling priority of a process.

It's a user-adjustable value that suggests to the kernel how "nice" a process should be to other processes when competing for CPU time.

## 🗝️ Key concepts

- A nice value ranges from `-20` to `+19`
- A higher nice value means a lower priority
- The default nice value for a newly started process is usually `0`
- A user can only increase the nice value of their own processes

## 🪛 Usage

- Start a new command with a specified nice value:

```bash
nice -n <nice_value> <command>
```

- Change the nice value of an already running process:

```bash
renice -n <nice_value> -p <PID>
```