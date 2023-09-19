# Process Monitoring Cheat Sheet

## [ps command](https://www.sysadmin.md/ps-cheatsheet.html) 

### Show all processes
  `ps aux`

### Show all processes including commandline arguments
  `ps -AFl`

### Show all processes with threads in tree mode
  `ps -AlFH`

### Show processes in hierarchy
  `ps -e -o pid,args --forest`

### Show list of processes awned by a specific user
  `ps -U user -u user u`

### Show information for a particular process
  `ps -p pid`
  `ps uax | grep process_name`

### Show all threads for a particular process by id
  `ps -p pid -L -o pid,tid,pcpu,state,comm`

### Get top 5 processe by CPU usage
  `ps -e -o pcpu,cpu,nice,state,cputime,args --sort pcpu | sed '/^ 0.0 /d'| tac |head -5`
  `ps auxf | sort -nr -k 3 | head -5`

### Get top 5 processes by memory usage
  `ps -e -orss=,args= | sort -b -k1,1n | pr -TW$COLUMNS| tac | head -5`
  `ps auxf | sort -nr -k 4 } head -5`

### Get secuirt info
  `ps -eo euser,ruser,suser,fuser,f,comm,label`

## [top command](https://gist.github.com/ericandrewlewis/4983670c508b2f6b181703df43438c37)

`h` shows help on interactive commands. Also see the [top manual page](http://man7.org/linux/man-pages/man1/top.1.html)

`q` to quit the program.

### Navigating

`Up` and `Down` to scroll through processes one by one, or `PageUp` and `PageDown` for paged navigation. 

`Left` and `Right` to navigate horizontally through fields (in case you're displaying a bunch).

`Shift+c` will show an index of where you are in the process list (eg 30/300 when your cursor is on process 30 and there are 300).

### Sorting 

`Shift+p` sort processes by CPU usage

`Shift+m` sort processes by memory usage

`Shift+r` reverse sort order

Sort on any field: Press `f` to bring up the Field Management menu. Select the field to sort on, press `s` and then `Escape`.

### Searching

`Shift+l` search for a string and highlights all occurences

`o` add a filter to limit which processes are displayed. A filter takes the format `{field name}{comparator}{value}`. For example, to see only processes owned by my user, I would add a filter `USER=eric`.

`Ctrl+o` view active filters.

`=` clear all filters.

### Other stuff

`m` switches memory views between the list of metrics and graph view.

`k` kill a process

`d` set the refresh rate (in seconds)

`Shift+w` saves the settings you've configured while running top to a file (`.toprc`) so they persist next time you use it.

`Shift+e` toggle the scale of memory metrics (between kilobytes and megabytes etc.) in the system memory summary, and `e` toggles the scale of memory metrics in the process list. The default is kilobytes, I find megabytes a useful level.

## [htop command](https://www.maketecheasier.com/power-user-guide-htop/)

## [lsof command](https://neverendingsecurity.wordpress.com/2015/04/13/lsof-commands-cheatsheet/)
