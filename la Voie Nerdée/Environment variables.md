An *environment variable* is a named object that contains data used by one or more applications.
They provide a simple way to share configuration settings between multiple applications and processes in Linux.

## A few key points to keep in mind

- Environment variables follow `<NAME>=<VALUE>` formatting
- They can be specified by separating values with colons:
  `<NAME>=<VALUE1>:<VALUE2>:<VALUE3>`
- Environment variables are case-sensitive

## Usage

- List all current environmental variables:
```bash
printenv
```

- Define a variable:
```bash
# for the current session:
export <VARIABLE>=<VALUE>
```

To define it permanently, add the line above to the `~/.bash_profile` or `~/.zshenv` and reload the shell

- Display a variable:
```bash
echo $VARIABLE
```

- Run a command under a modified environment
  (without affecting any global environment variables):
```bash
env <VARIABLE>=<VALUE> <command>
```




[^1]: Sources:
	https://www.cherryservers.com/blog/how-to-set-list-and-manage-linux-environment-variables
