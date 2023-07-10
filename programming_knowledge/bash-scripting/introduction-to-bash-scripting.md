# Introduction to Bash Scripting

Bash (or shell) scripting is a great way to automate repetitive tasks and can save you a ton of time as a developer. Bash scripts execute within a Bash shell interpreter terminal. Any command you can run in your terminal can be run in a Bash script. When you have a command or set of commands that you will be using frequently, consider writing a Bash script to perform it.

There are some conventions to follow to ensure that your computer is able to find and execute your Bash scripts. The beginning of your script file should start with `#!/bin/bash` on its own line. This tells the computer which type of interpreter to use for the script. When saving the script file, it is good practice to place commonly used scripts in the `~/bin/` directory.

The script files also need to have the “execute” permission to allow them to be run. To add this permission to a file with filename: `script.sh` use:

```bash
chmod +x script.sh
```

Your terminal runs a file every time it is opened to load its configuration. On Linux style shells, this is `~/.bashrc` and on OSX, this is `~/.bash_profile`. To ensure that scripts in `~/bin/` are available, you must add this directory to your PATH within your configuration file:

```bash
PATH=~/bin:$PATH
```

---

## Hello World

`script.sh`

```bash
#!/bin/bash

echo "Hello World!"
```

In the terminal run: `./script.sh`
