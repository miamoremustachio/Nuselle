An *exit code* (also known as an *status code*) is a numerical value returned by a command or script to indicate the outcome of its execution.

Code `0` generally indicates a successful result; anything other than `0` is considered an error.

The `?` environment variable contains info about the exit status of the previous command.

# 🔀 Condition chaining

| *Operator* | *Name*    | *Meaning*                                             |
| ---------- | --------- | ----------------------------------------------------- |
| `&&`       | AND       | executes only if the previous command is a success    |
| `︱︱`       | OR        | executes only if the previous command is a failure    |
| `;`        | Separator | executes regardless of status of the previous command |

