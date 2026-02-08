A *shebang* (`#!`) is the first line in a Unix-like scripts that tells the operating system which interpreter to use for executing the file (e.g., `#!/bin/bash` for [[bash]] or `#!/usr/bin/env python3` for Python).

It ensures script portability and allows scripts to be run as executables without explicitly calling the interpreter.

## `#!/bin/bash` vs `#!/usr/bin/env bash`

The primary difference between `#!/bin/bash` and `#!/usr/bin/env bash` is *specificity* versus *portability*.

`#!/bin/bash` hardcodes the path directly to the Bash interpreter, while `#!/usr/bin/env bash` uses the system's `PATH` [[environment variables|environment variable]] to locate the interpreter, making it more flexible across different systems.

- For system-critical scripts runs with elevated privileges, using the hardcoded path is more secure because the interpreter's location cannot be easily manipulated by a user's custom `PATH` variable