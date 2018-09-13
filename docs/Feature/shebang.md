Much like bash scripts or python scripts, blz can contain a 1 line shebang at the top of the file to tell a shell which program to use when running the script.

Include `#!/usr/bin/env blz` at the top of your blz script.

Now you can directly execute the script from a shell, without including the `blz` command.

I.E. `./myscript.blz` rather than `blz myscript.blz`