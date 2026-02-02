# FILE SYSTEM --- /,/tmp,/opt/,/sbin,/bin,/mnt,/lib,/etc,/var,/home,/boot,/media/,/sys,/dev,/usr,/srv

/ --- root directory All other directories are its subdirectories.

/tmp --- its a temprovary directory where everyone has full access which consists of the temrovary files.
Files here are usually deleted on reboot or periodically by the system

/opt --- its a optional directory so whenever any 3rd party apps need to be installed make sure this directory
eg: apache,nginx

/sbin --- which basically consists of all the system binaries where only the admins have acces to use these
eg: shutdown , reboot (these can be run by using sudo untill or unless that user has the sudo permission )

/bin --- which is also consists of system binaries but any one can use this 
eg: ls, pwd 

/mnt --- this can be used to temrovary mount the disk or the external devices 

/lib --- which actually has the library of all the applications installed like java,apache,etc

/etc --- which basically has the configuration of the installed apps or the users so if any necessary configuration needs to be changed we use this directory 
eg: getent passwd

/var --- which itself says variable like the files inside these folders are not permanent they keep on changing eg: logs 
eg: /var/log

/home --- users home that is user stores personal settings here 
eg: /home/ec2-user

/boot --- contains the boot loading content 

/media --- has the mountpoints of external removable disk like usb devices

/sys --- has kernel information

# importance of /etc/hostname 

basically the output what you see " ec2-user@ip-172-31-32-50 " this content is present inside /etc/hostname if you need to change the hostname permanently you can edit this file save the changes as well 

# A web application service called 'myapp' failed to start after a server reboot. What commands would you run to diagnose the issue?
approach 
- check with the service status ( sudo systemctl status service_name )
- check whether the service is been enabled or not ( sudo systemctl is-enabled service_name )
- check the logs using ( journalctl -u service_name )
- check with process name ( ps -eaf | grep <process_name> )
- check with the port number of the perticular service ( ss -tulpn | grep port number )
- sample snapshot of nginx service
  <img width="1917" height="859" alt="Screenshot 2026-02-01 224117" src="https://github.com/user-attachments/assets/3afd044c-a4b3-444e-a2c6-3c498be9b8ac" />


# Your manager reports that the application server is slow. You SSH into the server. What commands would you run to identify which process is using high CPU?
approach
- use top/htop to find out the CPU usage and find the PID
- check with the priority of the process if possible will try to change the priority of that process using renice
- Limit CPU usage by cpu limit -p PID -l 50 ( limit or helps in throttling of the process ) 
- if this process is not major then we can kill it usig kill PID or kill -9 PID
- try to take the snapshot that helps if there required you to do the soft or hard restart
- if needed we can change the instance type
- sample snapshot of cpu and process listing using htop or sorting by cpu 
<img width="1917" height="1014" alt="Screenshot 2026-02-01 224311" src="https://github.com/user-attachments/assets/038ad423-d747-4f4f-abfb-863de7615194" />
<img width="951" height="164" alt="Screenshot 2026-02-01 224416" src="https://github.com/user-attachments/assets/5bd1c34a-1a83-4b75-b34e-3cb562cc255e" />


# A developer asks: "Where are the logs for the 'docker' service?" The service is managed by systemd. What commands would you use?
approach 
- we will go inside /var/log/docker we can use tail -50 /var/log/docker 
- we can check using journalctl -u docker
- ps -aux --sort=%cpu |grep -i docker
- use top and check with the memory and CPU % of the process

# A script at /home/user/backup.sh is not executing. When you run it: ./backup.sh You get: "Permission denied" What commands would you use to fix this?
approach 
- try to check the file permission using long list ls -ll in that path
- for execution of the script ensure having +x permission ( chmod +x file_name )
- while executing ./file_name need an extra permission of +x but if you are executing file using sh file_name.sh or bash file_name.sh
- sample snapshot
<img width="678" height="596" alt="Screenshot 2026-02-02 133541" src="https://github.com/user-attachments/assets/88adfd74-19df-4e84-b0dc-0a6c71c7354f" />




