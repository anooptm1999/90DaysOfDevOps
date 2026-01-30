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

# file level
ls -a --- list the hidden files and folder 
rm --- remove file 
rm -r --- remove directory recursively ( used in deleting directory )
echo --- print something echo "hi" prints hi in terminal
tac --- to print the reverse order of the file content
mv --- used to rename as well can used to cut paste
mv abc.sh aaa.sh  ( re-naming )
mv /abc/abc.sh /bbc/ccc/ ( cut paste happens here )
head --- to print first 10 lines of file
tail --- to print bottom 10 lines of the file
cp --- copy from src to dest
chmod --- change file or folder permission 
chown --- change ownership of file or folder


# files editor 
cut -d " " -f1 filename --- printing the first column content but cannot be used in case of row operations
awk -f " " '{print $1}' --- printing the first column using feild space
awk 'NR==4 && NR==6' --- printing the rows entity as well
sed - stream editor to replace a pattern from file
sed -i "old pattern/new pattern/ig" file name / sed "old pattern/new pattern/ig" file name
grep pattern filename | wc -l --- pattern matching and counting total number of lines
uniq --- will pick only the unique patterns 
sort --- will sort the pattrens based on the sequence


# system config 
free -h --- RAM utilization
df -h --- disc utilization
nproc --- to see how many cores of cpu 
hostname -I --- gives the private ip of the server
curl ifconfig.me --- gives the public ip of the server
uptime --- to check about the server load 
date --- to see the date 
du -sh --- gives the file/directory size
uname -a --- shows the kernel version, pvt ip, public ip, architrecture type 


# networking 
netstat -a --- gives all the available ports of allocated and are free
netstat -l --- gives all the listening ports 
netstat -tulnp --- gives only the allocated ports 
ping 0 --- packet internet groper send 4 packets to check the availability or rediness of self server [TCP handshake syn ack syn---ack]
ping 8.8.8.8 --- check whether the perticular server has access to internet or not
traceroute --- will give how many hops it have taken to hit the destination server from host 
ss --- socket statistics 
ss -a --- kind of net tool but it is other version of netstat -a 
ss -p --- kind of net tool but it is other version of netstat -tulnp
ss -l --- kind of net tool but it is other version of netstat -l
dig --- help in checking the nameserver of the ip address


















