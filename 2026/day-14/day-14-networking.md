# OSI and TCP/IP Model
# OSI 1970's
- A application - end-user
- P presentation - encryption/ how the data is been shown 
- S session - unique connection establishment 
- T transport - TCP/UDP 
- N network - IP 
- D data-link - internet (ISP)
- P physical - information excahnge or bits wise 0,1

# TCP/ IP modela
- A application
- T transport
- I internet
- N network

- Identity: hostname -I (or ip addr show) — note your IP.
- Reachability: ping <target> — mention latency and packet loss.
- Path: traceroute <target> (or tracepath) — note any long hops/timeouts.
- Ports: ss -tulpn (or netstat -tulpn) — list one listening service and its port.
- Name resolution: dig <domain> or nslookup <domain> — record the resolved IP.
- HTTP check: curl -I <http/https-url> — note the HTTP status code.
- Connections snapshot: netstat -an | head — count ESTABLISHED vs LISTEN (rough).


<img width="1818" height="979" alt="Screenshot 2026-02-09 173455" src="https://github.com/user-attachments/assets/248fcf9a-26f9-4896-b980-98114e4dd5b9" />
<img width="1087" height="969" alt="Screenshot 2026-02-09 173509" src="https://github.com/user-attachments/assets/78abe790-f091-45c9-97d1-42fe9914ef84" />
<img width="1283" height="966" alt="Screenshot 2026-02-09 173531" src="https://github.com/user-attachments/assets/9fa7dd62-22ff-43e0-b20a-e8229a73fd77" />
<img width="1173" height="957" alt="Screenshot 2026-02-09 173611" src="https://github.com/user-attachments/assets/21a6617a-7c84-4302-a6b5-17875f121c52" />







