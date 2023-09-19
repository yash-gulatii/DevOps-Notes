## 19 September 2023

# [Bash Scripting](https://www.freecodecamp.org/news/bash-scripting-tutorial-linux-shell-script-and-command-line-for-beginners/)

## Introduction to Bash Scripting

### Bash Scripting - 
A bash script is a file containing a sequence of commands that are executed by the bash program line by line. It allows you to perform a series of actions, such as navigating to a specific directory, creating a folder, and launching a process using the command line.

By saving these commands in a script, you can repeat the same sequence of steps multiple times and execute them by running the script.

### Advantages of Bash Scripting

Bash scripting is a powerful and versatile tool for automating system administration tasks, managing system resources, and performing other routine tasks in Unix/Liux systems. Some advantages of shell scripting are:

- **Automation**: Automation can save time and reduce errors that can occur with maual execution and also reduce human errors.

- **Portability**: Shell scripts can run on various operating system like Unix, Linux, macOS ad even windows through the use of Virtual Machines or Emulators.

- **Flexibility**: Highly customizable and can be modified varing on the system requirements. Can be combied with other programming languages so that a more powerful script can be created.

- **Accessibility**:Easy to write/edit using any basic text editor and most os can execute using built-in shell interpreter.

- **Integration**: Can be integrated with other tools like databases, web server, and cloud services allowing to create more complex automation and management tasks.

- **Debugging**: Easy to debug, most shells have built-in debugginng and error-reporting tools to find bugs and fix them quickly.

### Shell vs Bash

The terms `shell` and `bash` are used interchangeably. But there is a subtle difference between the two.

The term `shell` referes to a program that provides a command-line interface for interacting with an operating system. `bash` (Bourne-Again SHell) is one of the most commonly used Unix/Linux shells and is the default shell in many Linux Distributions.

`$` is waiting for a command from normal user in command line/terminal.

`#` is waiting for a command from a superuser(root/administrator) in command line/terminal.

Bash is a type of shell, there are other shells available as well, such as Korn shell(ksh), C shell(csh), Z shell(zsh). Each shell has its own sytax ad set of features, but they all share the common purpose of providing a command-line interfaace for interacting with the operating system.

You can see your shell using `ps` command.

### Running Command in Termial

`date`: Displays the curret date.

`pwd`: Displays the present working directory.

`ls`: Lists the contents of the current directory.

`echo`: Prinnts a string of text, or value of a variable to the terminal.

`man`: Manual for any command.

### How to Create and Execute Bash Scripts

**Script naming conventions**
By naming convention, bash scripts end with `.sh`. However, bash scripts can run perfectly fine without the `sh` extension.

**Addig the Shebang**
Bash scripts start with a `shebang`. Shebang is a combiation of `bash #` and `bang !` followed by the bash shell path. This is the first line of the script. Shebang tells the shell to execute it via bash shell. Shebang is simply an absolute path to the bash interpreter.

Below is an example of the shebang statement.

```bash
#!/bin/bash
```

You can find your bash shell path using this command:

```bash
which bash
```

### Creating our first bash script

Create a file named `run_all.sh` using the `vi` command.

```bash
vi run_all.sh
```

> use `i` to get inn insert mode in vi and press `Esc` to get into command-mode and then type `:wq` to save and quit from vi.

### Executing the bash script

To make the script executable, assign execution rights to your user using this command:

```bash
chmod u+x run_all.sh
```

Here,
- `chmod` Modifies the ownership of a file
- `u` is for the current user
- `+x` is for execution rights
- `run_all.sh` is the File

## Bash Scripting Basics

### Comments in bash scripting

Comments start with a `#` in bash scripting. This means that any line that begin with `#` is a comment and will be ignored by the interpreter.

Comments are used to document the code and to give more understanding to the reader.

```bash
# This is an example comment
```

### Varaibles and data types in Bash

Variables let you store data. You can use variables to read, access, and manipulate data troughout your script.

There are no data types in Bash. In Bash, a variable is capable of storing numeric values, individual characters, or strings of characters.

Assign the values directly:

```bash
country=India # Creating a Variable

echo $country # Accessing the Variable
``` 

### Variable naming conventions
