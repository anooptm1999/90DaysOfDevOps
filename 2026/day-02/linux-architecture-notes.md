# Linux Architecture

A shortcut to remember the Linux architecture is {ASKH}

A – Application

S – Shell

K – Kernel

H – Hardware

Example:
When a user enters the date command in the CLI, the command acts as an application.
The shell interprets the command and sends a request to the kernel.
The kernel executes the required binary (located in /bin or /sbin for administrative commands) and interacts with the hardware to fetch the system time.
The output is then sent back to the shell and displayed on the CLI, where the user can read it.


# list of 5 regular using commands in daily life
ls ( to list the files or folder ) ls 

cd ( change the directory or path ) cd /home/ec2-user/

touch,mkdir ( make file or directory ) touch abc.sh

man ( it can be used to know how the command need to be used/ manual ) man awk Press q to quit

cat ( to see the contents of the file ) cat abc.sh


# PROCESS  New → Running → Waiting/Sleeping → Stopped → Zombie → Dead

Process is a temprovary task which has the pid can be seen using the command ps,ps -eaf or if it related to perticular user then use ps -u username.
like eg: if we use mkdir abc (creation of folder) that is a termprovary task which is been assigned with pid (process id ).

Once a process starts, it enters the running state.
majorly the process runs in the foreground, the terminal remains occupied until the process terminates.
To use the terminal for other tasks, the process can be run in the background using &, or suspended using Ctrl+Z and resumed with background.

There might be a chance that a parent process creates child processes.
If a child process finishes execution and the parent process does not call wait() to collect the child’s exit status, the child process becomes a zombie, shown as state Z.
The zombie process remains in the process table until the parent acknowledges it or terminates.

If a user need to give some waiting time or cooling time for process we can use sleep 10, or with required amount of seconds 

an abrupt stopping of process like using ctrl+z will make the perticular process into stopped state 

Dead is the final state, after which the process is completely removed from the kernel.

to terminate the process we can either go with gracefull approch or forcefull approach 

kill PID --- terminating the process gracefully 
kill -9 PID --- terminating the process forcefully 
pkill -u Username --- terminating all process by an user gracefully created 
pkill -9 -u Username --- terminating all process by an user forcefully created 


# Booting Sequence

BIOS  --- GRUB --- Kernel check the filemounts and hardware --- system files start to execute --- user able to see the terminal CLI

BIOS is a firmware (integrated chip) that performs POST (Power-On Self-Test) to check basic hardware (CPU, RAM, peripherals).
GRUB (or any bootloader) loads after BIOS.Look for Linux kernel image to load into memory.
Kernel is loaded into memory by GRUB.
Kernel initializes hardware, mounts the root filesystem, and sets up basic drivers.
Kernel then executes the first user-space process, usually SYSTEMD (PID 1) or init.
after systemd starts the necessary getty/login service, the user sees a terminal (CLI) or GUI if a display manager is enabled.






