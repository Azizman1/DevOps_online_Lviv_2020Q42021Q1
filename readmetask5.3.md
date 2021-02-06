Linux has basically 5 states: Running/Runnable (R): running processes are processes using a CPU core right now,
a runnable process is a process that has everything to run and is just waiting for a CPU core slot.


Using the pstree command:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.3/1.png
https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.3/2.png

Proc file system (procfs) is virtual file system created on fly when system boots and is dissolved at time of system shut down.
It contains the useful information about the processes that are currently running, it is regarded as control and information centre for kernel.


Printing information about the processor:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.3/3.png


Using the ps command to getting information about the proccess:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.3/4.png


User-space processes have its own virtual address space. Kernel processes or threads do not have their own address space, they operate within kernel address space only. 
And they may be started before the kernel has started any user process (e.g. init).


Printing the list of processes to the terminal:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.3/4.png


Printing processes of a specific user:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.3/5.png


For analyze existing running tasks, we can get this result by using a "ps -U usermane -u username" command:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.3/6.png


The top command displays processor activity of your Linux box and also displays tasks managed by kernel in real-time.
It'll show processor and memory are being used and other information like running processes.

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.3/7.png


Displaying the processes of the specific user using the top command:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.3/8.png


Interactive commands, that can be used to control the top command:

1) By pressing (Shift+O), we can sort field via field letter, for example press ‘a‘ letter to sort process with PID (Process ID);
2) By using ‘u‘ option, we can display specific user process details;
3) By using ‘z‘ option in running top command, we can display running process in color;
4) ‘c‘ option in running top command, it will display absolute path of running process;
5) We can kill a process after finding PID of process by pressing ‘k‘ option in running top command;
6) By pressing (Shift+P), we can sort processes as per CPU utilization.


Sorting the contents of the processes window:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.3/9png


We can change the process priority using nice and renice utility. Nice command will launch a process with an user defined scheduling priority.
Renice command will modify the scheduling priority of a running process.


We can use ‘r‘ option on the top command to change the priority of the process.


Using the kill command:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.3/10png


Using the jobs,fg,bg commands:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.3/11png

The fg command switches a job running in the background into the foreground.
The bg command restarts a suspended job, and runs it in the background. If no job number is specified, then the fg or bg command acts upon the currently running job.
The jobs command displays a list of current background tasks.
Sleep is a command which is used to create a dummy job which runs for define seconds.


Cheking the implementability of the most frequently used OPENSSH commands in the MS Windows. Implementing basic SSH settings:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.3/12png


Implementing 3 different keys with different algorithms for encryption in SSH:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.3/13.png


Implementing port forwarding for the SSH client from the guest Linux virtual machine to the host machine behind NAT:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.3/14.png

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.3/15.png


After doing this task, i examine couple of commands in Linux OS and i acquanted with OpenSSH technology.
