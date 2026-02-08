In Linux, input and output operations between a program and its environment are managed through standard *I/O streams*.

There are 3 types of I/O connections:
## standard input (*stdin*)

- A stream which program reads data from
- Use `0` file descriptor

## standard output (*stdout*)

- A stream which program writes data to
- Use `1` file descriptor

## standard error (*stderr*)

- A stream which program writes error messages to
- Use `2` file descriptor

![[standard-stream.png]]

# 🚏 Redirection

| *Operator* | *Meaning*                                                 |
| ---------- | --------------------------------------------------------- |
| `>`        | Redirect to a file or another stream (overwrite data)     |
| `>>`       | Redirect to a file or another stream (append data)        |
| `2>`       | Redirect to a file or another stream (use stream `2`)     |
| `2>&1`     | Redirect stream `2` to the same destination as stream `1` |
| `<`        | input data from a file                                    |
| `<<`       | input data from another input (line by line)              |
| `<<<`      | input data from a string                                  |
| `︱`        | Pipe to another command                                   |
# 🫖 tee

To write the standard input to both standard output and one or more files, use `tee` command:

```bash
<program> | tee -a output.txt

# -a flag stands for append
# (tee replaces the content of the target file by default)
```





[^1]: Sources:
	https://zedas.fr/posts/linux-explained-6-standard-streams/
