COMMAND 1 :uptime

OUTPUT:13:09:56 up  9:15,  1 user,  load average: 0.07, 0.09, 0.09

EXPLANATION:This command displays the time elapsed since the system was last booted.
It also shows the number of logged-in users and the load average.
The output indicates that the system has been running for more than nine hours with low load.

COMMAND 2:ps -u $USER

OUTPUT:PID TTY          TIME CMD
279 pts/0    00:00:00 bash
323 ?        00:00:01 systemd
324 ?        00:00:00 (sd-pam)
348 pts/1    00:00:00 bash
172428 pts/0 00:00:00 ps

EXPLANATION:This command lists all processes currently running under the logged-in user.
It shows process IDs, terminal information, CPU time, and command names.
Only processes owned by the user are displayed.


COMMAND 3:top

OUTPUT:PID USER %CPU COMMAND
172651 adhvaitha 1.2 top

EXPLANATION:This command displays real-time information about system processes.
From the output, the top process itself is consuming the highest CPU.
It helps identify CPU-intensive processes.


COMMAND 4:sleep 300 &

OUTPUT:[1] 173748

EXPLANATION:This command starts a process in the background using the ampersand operator.
The output shows the job number and process ID.
This confirms that the command was executed in the background.

COMMAND 5:renice 5 -p 2154

OUTPUT:renice: failed to get priority for 2154 (process ID): No such process

EXPLANATION:This command attempts to change the priority of a running process.
The output indicates that the specified process was no longer active.
Priority changes can only be applied to currently running processes.


COMMAND 6:free -h

OUTPUT:total        used        free      shared  buff/cache   available
Mem:           3.7Gi       461Mi       3.0Gi       3.6Mi       295Mi       3.2Gi
Swap:          1.0Gi          0B       1.0Gi

EXPLANATION:This command displays memory usage in a human-readable format.
It shows total, used, free, and available memory.
The output indicates sufficient free memory on the system.


COMMAND 7:df -h ~

OUTPUT:Filesystem      Size  Used Avail Use% Mounted on
/dev/sdd       1007G  1.3G  955G   1% /

EXPLANATION:This command displays disk usage of the filesystem containing the home directory.
It shows total size, used space, and available space.
The output confirms that there is enough disk space available.


COMMAND 8:echo $SHELL

OUTPUT:/bin/bash

EXPLANATION:This command displays the name of the shell currently in use.
The output confirms that Bash is the active shell.
Bash is the default shell on most Linux systems.


COMMAND 9:uname -a > system_report.txt

OUTPUT:[1]+  Done                    sleep 300

EXPLANATION:This command redirects system information into a file named system_report.txt.
The terminal output shows completion of the background sleep process.
System details are saved in the file instead of being displayed on the screen.


COMMAND 10:ncdu ~

OUTPUT:ncdu: command not found

EXPLANATION:This command attempts to run the ncdu disk usage visualization tool.
The output indicates that ncdu is not installed on the system.
Since system configuration changes are not allowed, the tool was not installed.


