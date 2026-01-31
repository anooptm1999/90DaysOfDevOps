# recording the output of CPU, memory, logs and service analysis
# top
<img width="1918" height="951" alt="Screenshot 2026-01-31 021126" src="https://github.com/user-attachments/assets/981195df-5788-4595-b98f-f8689458ccd3" />

# htop
<img width="1915" height="1020" alt="Screenshot 2026-01-31 021334" src="https://github.com/user-attachments/assets/55b8256b-19f8-4337-8bd0-644740c2580a" />

# service analysis
<img width="1919" height="1013" alt="Screenshot 2026-01-31 021521" src="https://github.com/user-attachments/assets/25817304-af82-4c85-bb23-db15fca45223" />

# logs analysis
<img width="1919" height="1018" alt="Screenshot 2026-01-31 021707" src="https://github.com/user-attachments/assets/85732f97-0531-49df-988a-3d0b4027964f" />
<img width="1915" height="1017" alt="Screenshot 2026-01-31 021729" src="https://github.com/user-attachments/assets/c8d148ed-5061-45a0-8248-6a7ab2b1ee76" />
<img width="1523" height="196" alt="Screenshot 2026-01-31 021825" src="https://github.com/user-attachments/assets/364147e0-7655-47a3-a309-90bca01b0703" />
<img width="1915" height="963" alt="Screenshot 2026-01-31 022221" src="https://github.com/user-attachments/assets/35639b97-fe9c-44a9-8d9c-bcbcf269b042" /> 
<img width="1919" height="1017" alt="Screenshot 2026-01-31 022349" src="https://github.com/user-attachments/assets/87ce6fc6-bd6b-4289-bed7-d0f1577fdba5" />
<img width="1919" height="1017" alt="Screenshot 2026-01-31 022429" src="https://github.com/user-attachments/assets/9ec350c1-0d83-4d1a-91c7-f3d8a8e31dfc" />
<img width="1909" height="1010" alt="Screenshot 2026-01-31 023940" src="https://github.com/user-attachments/assets/c43aeb3d-6a55-4a6c-ba7e-4cda2d052ad4" />
<img width="1919" height="1010" alt="Screenshot 2026-01-31 024141" src="https://github.com/user-attachments/assets/0700c5c7-3d35-4986-89e0-464e965805e1" />

# os analysis
<img width="1919" height="704" alt="Screenshot 2026-01-31 023056" src="https://github.com/user-attachments/assets/564833ea-ae4c-4e3d-a200-c33b4d365f25" />
<img width="1336" height="305" alt="Screenshot 2026-01-31 023229" src="https://github.com/user-attachments/assets/b821b500-99e5-47c2-8f2a-cb03557bd494" />
<img width="1281" height="701" alt="Screenshot 2026-01-31 023524" src="https://github.com/user-attachments/assets/b3c793d6-2887-4b27-9e2a-6d431914d33c" />


# approach of high cpu usage 

- use either top or htop to see what percentile of CPU is utilizing
- check with the PID and the priority of the task
- if it is of some less prior we can either use the deprioritizing to provide the cooling period
- or else this process can be stopped or killed by using kill PID or kill -9 PID (forcefully avoid this before using this take permission)
- if its a critical process then be sure take the snapshots
- if possible try to make the soft reboot of the process or restart 
- try to change the priority of that perticular process
- if required enhance or resize the CPU

# for disk

- there might be chances of large un-used files try to make sure finding those using find /path/ -type f -mtime +30 you can delete those based on the discussion
- try to make the log rotration
- if required make sure using of compressing the large files using tar -cvzf name.log.gz large_file1 large_file2

# for service 

- check whether the service state by sudo systemctl status service_name
- if that is up and running try to use restarting that service gracefully sudo systemctl restart service_name
- please check the other componets as RAM, disk and cpu usage
- please do read the log files of the service using journalctl -u service_name



















