# creation of instance and connecting via SSH 
- use windows+r (cmd in run ). change the path from c:dekstop to downloads
- use git bash ( best )
- if you have local linux no worries
- try running command ssh -i "private key.pem" username@hostname set the permission to readonly of pvt_key.pem
- then we were into the server
a sample snap is been given below

<img width="1556" height="622" alt="Screenshot 2026-02-02 190658" src="https://github.com/user-attachments/assets/78b44cd0-b28b-4841-8ed8-660897bb888b" />


# installing the nginx and checking the service is up or not 
make sure updateing the packages soon after doing ssh ( sudo yum update / upgrade )
- here I had used amazon linux 2023 server so package manager is yum if you are using some other like (ubuntu:apt RHEL:dnf )
- then use sudo yum install nginx -y, start the service ( sudo systemctl start service_name ) check the status ( sudo systemctl status nginx )
- It will show ( active and running ) then your service is up and running
- hit the public_IP:80 so that you can see the welcome page
- make sure opening the port 80 for this service
 a sample snap is been given below

 <img width="1626" height="784" alt="Screenshot 2026-02-02 195124" src="https://github.com/user-attachments/assets/d74df7e1-63d5-4536-84bf-17e6a722650a" />
 # installing the package
 <img width="1919" height="981" alt="Screenshot 2026-02-02 191123" src="https://github.com/user-attachments/assets/6c5407c4-84e4-4d51-a0d3-fe0a92bd4d71" />
 # status checking 
 <img width="1626" height="784" alt="Screenshot 2026-02-02 195124" src="https://github.com/user-attachments/assets/54c7bf16-77a2-4121-bb83-d36fce90e6ec" />
 # smaple o/p of welcome page of NGINX
 <img width="1919" height="968" alt="Screenshot 2026-02-02 190856" src="https://github.com/user-attachments/assets/ed09a8d6-c5fd-490a-95a1-45ca993a25cf" />

# copying the logs of NGINX from EC2 --- local 
- have a git bash opened and redirect your path where there is a downloaded private key of that server
- by using scp ( secure copy ) i,e scp -i pvt-key.pem username@hostname of EC2-server:path-of-the-logfile-in-EC2 local-machine-path
- (( scp -v -i pvt-key.pem username@hostname:/home/ec2-user/nginx-logs.txt ~/Desktop/ ))
- -v represents verbose is nothing but visually it will show all the process how?how?what?
sample snaps are attached

<img width="1130" height="989" alt="Screenshot 2026-02-02 194058" src="https://github.com/user-attachments/assets/e203dcb4-233c-4849-85ce-3e6b7716356e" />
<img width="1027" height="971" alt="Screenshot 2026-02-02 194116" src="https://github.com/user-attachments/assets/64ef1e5f-d8dd-4bcd-a6a3-ab828b665bab" />

# viewing log file in local 
<img width="1919" height="654" alt="Screenshot 2026-02-02 194256" src="https://github.com/user-attachments/assets/f2b7b3b1-3383-479f-8f4a-af1b5ef10854" />









