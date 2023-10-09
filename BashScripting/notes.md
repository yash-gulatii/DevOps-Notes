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

In Bash scripting, the following are the variable naming conventions:

1. Variable names should start with a letter or an underscore(`_`).
2. Variable names can contain letters, numbers, and underscores(`_`).
3. Variable names are case-sensitive.
4. Variable names should not contain spaces or special characters.
5. Use descriptive names that reflect the purpose of the variable.
6. Avoid using reserved keywords, such as `if`, `then`, `else`, `fi`, and so onn as variable names.

Here are some examples of valid variable names in Bash:

```
name
count
_var
myVar
MY_VAR
```

And here are some examples of invalid variable names:

```
2ndvar (variable name starts with a number)
my var (variable name contains a space)
my-var (variable name contains a hyphen)
```

Following these naming conventions helps make Bash scripts more readable and easier to maintain.

### Input and output in Bash scripts

##### Gathering input

In this section, we'll discuss some methods to provide input to our scripts.

1. Reading the user input and storing it in a variable.

We can read the user input using the `read` command.

``` bash
#!/bin/bash
echo "Today is" `date`

echo -e "\nEnter the path to directory"
read the_path

echo -e "\nYour path has the following files and folders: "
ls $the_path
```

2. Reading from a file

This code reads each line from a file named `input.txt` and prints it to the terminal. We'll study while loops later.

``` bash
while read line
do
	echo $line
done < input.txt
```

3. Command lie arguments

In a bash script or function, `$1` denotes the initial argument passed, `$2` denotes the second argument passed, and so forth.

This script takes a name as a command-line argument and prints a personalized greeting.

``` bash
echo "Hello, $1!"
```

##### Displaying output
Here we'll discuss some methods to receive output from the scripts.

1. Printing to the terminal:

```
echo "Hello, World!"
```

This prints the text "Hello, World!" to the terminal.

2. Writing to a file:

```
echo "This is some text." > output.txt
```

This writes the text "This is some text." to a file named `output.txt`. Note that the `>` operator overwrites a file if it already has some content.


3. Appending to a file:

```
echo "More text." >> output.txt
```

This appeds the text "More text." to the end of the file `output.txt`.

4. Redirecting output:

```
ls > files.txt
```

This lists the files in the current directory and writes the output to a file named `files.txt`. You can redirect output of any command to a file this way.

### Basic Bash commands (echo, read, etc.)

Here is a list of some of the most commonly used bash commands:

1. `cd`: Change the directory to a different location.
2. `ls`: List the contents of the current directory.
3. `mkdir`: Create a new directory.
4. `touch`: Create a new file.
5. `rm`: Remove a file or directory.
6. `cp`: Copy a file or directory.
7. `mv`: Move or rename a file or directory.
8. `echo`: Print text to the terminal.
9. `cat`: Concatenate and print the contents of a file.
10. `grep`: Search for a pattern in a file.
11. `chmod`: Change the permissions of a file or directory.
12. `sudo`: Run a command with administrative privileges.
13. `df`: Display the amount of disk space available.
14. `history`: Show a list of previously executed commands.
15. `ps`: Display information about running processes.

### Conditional statements (if/else)

Expressions that produce a boolean result, either true or false, are called contitions. There are several ways to evaluate conditions, including `if`, `if-else`,`if-elif-else`, and nested conditionals.

**Syntax:**

``` bash
if [[ condition ]];
then
	statement
elif [[ condition ]]; then
	statement
else
	do this by default
fi
```
> Syntax of bash conditional statemets

We ca use logical operators such as AND `-a` and OR `-o` to make comparisons that have more significance.

```
if [ $a -gt 60 -a $b -lt 100 ]
```
> This statement checks if both conditions are `true`: a is greater than 60 AND b is less than 100.


Let's see an example of a Bash script that uses `if`, `if-else`, and `if-elif-else` statements to determine if a user-inputted number is positive, negative, or zero:

```bash
#!/bin/bash

echo "Please enter a number: "
read num

if [ $num -gt 0 ]; then
	echo "$num is positive"
elif [ $num -lt 0 ]; then
	echo "$num is negative"
else
	echo "$num is zero"
fi
```
> Script to determine if a number is positive, negative, or zero

The script first prompts the user to enter a number. Then, it uses an `if` statement to check if the number is greater than 0. If it is, the script outputs that the number is positive. If the number is not greater than 0, the script moves on to the next statement, which is a `if-elif` statemet. Here, the script check if the number is less than 0. If it is, the script outputs that the number is negative. Finally, if the number is neither greater than 0 nor less than 0, the script uses an `else` statement to output that the number is zero.

### Looping and Branching in Bash

##### While loop

While loops check for a condition and loop until the condition remains `true`. We need to provide a counter statement that increments the counter to control loop execution.

In the example below, `(( i += 1 ))` is the counter statement that increments the value of `i`. The loop will run exactly 10 times.

```bash
#!/bin/bash
i=1
while [[ $i -le 10 ]]; do
	echo "$i"
	(( i += 1 ))
done
```
> While loop that iterates 10 times.

##### For loop

The `for` loop, just like the `while` loop. allows you to execute statements a specific number of times. Each loop differs in its syntax and usage.


In the example below, the loop will iterate 5 times.

```bash
#!/bin/bash

for i in {1..5}
do
	echo $i
done
```
> For loop that iterates 5 times.

##### Case statements

In Bash, case statements are used to compare a given value against a list of patterns and execute a block of code based on the first pattern that matches. The syntax for a case statement in Bash is as follows:

```
case expression in
	pattern1)
		# code to execute if expression matches pattern1
		;;
	pattern2)
		# code to execute if expression matches pattern2
		;;
	pattern3)	
		# code to execute if expression matches pattern3
		;;
	*) 
		# code to execute if none of the above patterns match expression
		;;
esac
```
> Case statements syntax

Here, "expression" is the value that we want to compare, and "pattern1", "pattern2", "pattern3", and so on are the patterns that we want to compare it against.

The double semicolon ";;" seperates each block of code to execute for each pattern. The asterisk "*" represents the default case, which executes if none of the specified patterns match the expression.

Let's see an example.

```
fruit="apple"

case $fruit in
	"apple")
		echo "This is a red fruit"
		;;
	"banana")
		echo "This is a yellow fruit"
		;;
	"orange")
		echo "This is an orange fruit"
		;;
	"*")
		echo "Unkown fruit"
		;;
esac
```
> Example of case statement

In this example, since the value of "fruit" is "apple", the first pattern matches, and the block of code that echoes "This is a red fruit". is executed. If the value of "fruit" were instead "banana", the second pattern would match and the block of code that echoes "This is a yellow fruit." would execute, and so on. If the value of "fruit" does not match any of the specified patterns, the default case is executed, which echoes "Unkown fruit."

### How to Schedule Scripts using cron

Cron is a powerful utility for job scheduling that is available in Unix-like operating systems. By configuring cron, you can set up automated jobs to run on a daily, weekly, monthly, or specific time basis. The automation capabilities provided by cron plat a crucial role inn Linux system administration.

Below is the syntax to schedule crons:

```
# Cron job example
* * * * * sh /path/to/script.sh
```

Here, the `*`s represent minute(s) hour(s) day(s) month(s) weekday(s), respectively.

Below are some examples of scheduling cron jobs.

|SCHEDULE | DESCRIPTION| Example |
|---------|------------|---------|
| `0 0 * * *` | Run a script at midnight every day | `0 0 * * * /path/to/script.sh` |
| `*/5 * * * *` | Run a script every 5 minutes | `*/5 * * * * /path/to/script.sh` |
| `0 6 * * 1-5` | Run a script at 6am from Monday to Friday | `0 6 * * 1-5 /path/to/script.sh` |
| `0 0 1-7 * *` | Run a script on the first 7 days of every month | `0 0 1-7 * * /path/to/script.sh` |
| `0 12 1 * *` | Run a script on the first day of every month at noon | `0 12 1 * * /path/to/script.sh` |
|-----------------|--------------------|-----------|

##### using crontab

The `cronntab` utility is used to add and edit the cron jobs.

`crontab -l` lists the already scheduled scripts for a particular user.

You can add and edit the cron through `crontab -e`.

### How to Debug and Troubleshoot Bash Scripts

Debugging and troubleshooting are essential skills for any Bash scripter. While Bash scripts can be incredibly powerful, they can also be prone to errors and unexpected behavior. In this section, we will discuss some tips and techniques for debugging and troubleshooting Bash scipts.

##### Set the `set -x` option

One of the most useful techniques for debugging Bash scripts is to set the `set -x` option at the beginning of the script. This option enables debuggig mode, which causes Bash to print each command that it executes to the terminal, preceded by a `+` sign. This can be incredibly helpful in identifying where errors are occurring in your script.

```bash
#!/bin/bash

set -x

# Your script goes here
```

##### Check the exit code

When Bash encounters an error, it sets an exit code that indicates the nature of the error. You can check the exit code of the most recent command using the `$?` variable. A value of `0` indicates success, while any other value indicates an error.

```bash
#!/bin/bash

# Your script goes here

if [ $? -ne 0 ]; then
	echo "Error occurred."
fi
```

##### Use `echo` statements

Another useful technique for debugging Bash scripts is to insert `echo` statements throughout your code. This can help you identify where errors are occurring and what values are being passed to variables.

```bash
#!/bin/bash

# Your script goes here

echo "Value of variable x is: $x"

# More code goes here
```

##### Use the `set -e` option

If you wwant your script to exit immediately when any command in the script fails, you can use the `set -e` option. This option will cause Bash to exit with an error if any command in the script fails, making it easier to identify and fix errors in your script.

```bash
#!/bin/bash

set -e

# Your script goes here
```

##### Troubleshooting crons by verifying logs

We can troubleshoot crons using the log files. Logs are maintaied for all the scheduled jobs. You ca check ad verify i logs if a specific job ra as iteded or not.

For Ubuntu/Debuan, you can find `cron` logs at:

` /var/log/syslog `

The location varies for other distributions.

A cron job log file can look like this:

```
2022-03-11 00:00:01 Task started
2022-03-11 00:00:02 Running script /path/to/script.sh
2022-03-11 00:00:03 Script completed successfully
2022-03-11 00:05:01 Task started
2022-03-11 00:05:02 Running script /path/to/script.sh
2022-03-11 00:05:03 Error: unable to connect to database
2022-03-11 00:05:03 Script exited with error code 1
2022-03-11 00:10:01 Task started
2022-03-11 00:10:02 Running script /path/to/script.sh
2022-03-11 00:10:03 Script completed successfully
```
> Cron log

