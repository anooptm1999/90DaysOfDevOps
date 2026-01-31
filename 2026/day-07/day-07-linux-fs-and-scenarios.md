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
