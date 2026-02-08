*System call* in Linux is an essential interface between user-space applications and the OS [[kernel]].

It allows programs to request access to privileged resources such as CPU, disk space and computer memory, network etc.

# Types of System Calls

## ⌛ Process control

- Managing the creation, execution, and termination of [[processes]]
- Examples: `fork()`, `exec()`, `exit()`

## 📁 File management

- Operations on files and directories
- Examples: `open()`, `read()`, `write()`, `close()`

## 🖨️ Device management

- Interacting with hardware devices and their buffers
- Example: `ioctl()`

## 📄 Information maintenance

- Accessing and setting system data, time, and configuration details
- Examples: `getpid()`, `alarm()`, `sleep()`

## 📠 Communication

- Facilitating inter-process communications (IPC) and network
- Examples: `pipe()`, `shmget()`, `mmap()`





[^1]: Sources:
	https://www.geeksforgeeks.org/linux-unix/linux-system-call-in-detail/
