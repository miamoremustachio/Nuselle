The *top* is a command-line system monitoring utility available on various UNIX systems.
It presents a real-time view of running [[processes]] along with overall resource usage details such as CPU load, memory consumption etc.

## 🧰 Main interface

### `top`

- Initial (summary) line
- Shows system time, uptime, number of users and load average
  *(the average number of processes waiting for CPU time over the last 1 minute, 5 minutes, and 15 minutes, respectively)*

### `tasks:`

- An overview of all [[processes]] currently managed by the system

### `%CPU(s):`

- Shows how the CPU time is distributed across different types of tasks:
	- `us` - Percentage of CPU time spent running ==us==er processes
	- `sy` - Percentage of CPU time spent running kernel (==sy==stem) processes
	- `ni` - Percentage of CPU time spent running processes with a [[nice|nice value]]
	- `id` - Percentage of CPU time spent ==id==le
	- `wa` - Percentage of CPU time spent ==wa==iting for I/O operations to complete
	- `hi` - Percentage of CPU time spent servicing ==h==ardware ==i==nterrupts
	- `si` - Percentage of CPU time spent servicing ==s==oftware ==i==nterrupts
	- `st` - Percentage of CPU time ==st==olen from the virtual machine by hypervisor

### `MiB Mem:`

- Provides detailed information about the RAM usage

### `MiB Swap:`

- Shows information about [[swap]] space usage

## 📑 List of processes

| *Column*  | *Meaning*                                        |
| --------- | ------------------------------------------------ |
| `PID`     | Task’s [[Processes#🪪 PID/PPID\|process id]]     |
| `USER`    | Task owner                                       |
| `PR`      | Process’ priority                                |
| `NI`      | Task's [[Nice\|nice value]]                      |
| `VIRT`    | Total virtual memory used by the process         |
| `RES`     | RAM used by the process (in `kb`)                |
| `SHR`     | Shared memory size used by the process (in `kb`) |
| `%CPU`    | CPU usage                                        |
| `%MEM`    | Memory usage                                     |
| `TIME+`   | CPU Time                                         |
| `COMMAND` | The name of the command that started the process |

## 🖥️ Usage

| *Shortcut*  | *Action*                                            |
| ----------- | --------------------------------------------------- |
| `s`         | Change update frequency                             |
| `1`         | Toggle the display of individual CPU cores          |
| `Shift + P` | Sorts processes by CPU usage (the default behavior) |
| `Shift + M` | Sorts processes by memory usage                     |
| `k`         | Enter a PID to kill a process                       |
