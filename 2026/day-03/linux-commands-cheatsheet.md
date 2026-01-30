# Process management

We alredy know what is process in our day 2 now how to monitor this yes by ps, ps -aux, ps -ef or ps -u username but we alredy have a pre written commands in linux like 
top or we have htop similer but GUI is great 

we can either set the priority for the process with nice or renice
Here while setting the priority for process we need to use the parameter of numericals from -20 to 19
least the number more the priority 

eg: nice -n -5 systemctl restart httpd you are setting the priority but if in case you need change the priority you can use 
    renice -n -10 systemctl restart httpd's PID

we do have the process need to run in foreground or background how to see the background running jobs as well 
jobs, fg, bg

jobs/jobs -l will give the job/job PID of process which went background so after that if you need to run that perticular process into foreground 
eg: fg %1 this will make that perticular process to run in foreground 
    bg %1 this will make that perticular process to run in background 


# add on commands 

# File Level
- ls -a --- list hidden files and folders
- rm --- remove file
- rm -r --- remove directory recursively
- echo "hi" --- print something (prints hi in terminal)
- tac --- print file content in reverse line order
- mv --- rename or move files/directories
- mv abc.sh aaa.sh --- rename file
- mv /abc/abc.sh /bbc/ccc/ --- move/cut-paste file
- head --- print first 10 lines of file
- tail --- print last 10 lines of file
- cp src dest --- copy file/directory
- chmod --- change file or directory permissions
- chown --- change ownership of file or directory
- chgrp --- change group ownership

# File Editors / Text Processing
- cut -d " " -f1 filename --- print first column (by delimiter)
- awk '{print $1}' filename --- print first column
- awk 'NR==4 || NR==6' filename --- print lines 4 and 6
- sed --- stream editor to replace patterns
- sed -i 's/old/new/g' filename --- replace pattern in file
- grep pattern filename | wc -l --- pattern matching and count lines
- uniq filename --- show unique lines
- sort filename --- sort lines alphabetically or numerically

# System Configuration
- free -h --- RAM utilization
- df -h --- disk utilization
- nproc --- number of CPU cores
- hostname -I --- show private IP of server
- curl ifconfig.me --- show public IP of server
- uptime --- server load and uptime
- date --- show current date and time
- du -sh file/dir --- show file or directory size
- uname -r --- kernel version
- uname -a --- full system info (kernel, hostname, architecture)

# Networking
- netstat -a --- show all sockets/ports
- netstat -l --- show listening ports
- netstat -tulnp --- show allocated TCP/UDP ports with PID
- ping 127.0.0.1 --- check local host connectivity
- ping 8.8.8.8 --- check internet connectivity
- traceroute <host> --- show hops from source to destination
- ss --- socket statistics
- ss -a --- show all sockets (netstat -a equivalent)
- ss -l --- show listening sockets (netstat -l equivalent)
- ss -p --- show process using sockets (netstat -tulnp equivalent)
- dig <domain> --- check DNS records (NS, A, MX, etc.)
- ip addr show --- show IP addresses of interfaces
- curl <url> --- test server response or download content




















