# Explain in 3–4 lines: what happens when you type google.com in a browser?
7️⃣ Application Layer
Browser creates an HTTP request for www.google.com.

6️⃣ Presentation Layer
Data is encrypted using TLS (HTTPS).

5️⃣ Session Layer
Session is established and maintained between your browser and Google.

4️⃣ Transport Layer
TCP creates connection (3-way handshake) and ensures reliable delivery.

3️⃣ Network Layer
IP adds source & destination IP address and routes packet across internet.

2️⃣ Data Link Layer
Frames are created using MAC addresses (used inside local network).

1️⃣ Physical Layer
Bits (0s and 1s) are sent as electrical signals / light / radio waves.

# What are these record types? Write one line each:
| Record | Maps To        | Used For               |
| ------ | -------------- | ---------------------- |
| A      | IPv4 (32-bit)  | Website hosting        |
| AAAA   | IPv6 (128-bit) | Website hosting (IPv6) |
| CNAME  | Another domain | Alias                  |
| MX     | Mail server    | Email routing          |
| NS     | DNS server     | Authority              |


# Run: dig google.com — identify the A record and TTL from the output
google.com.   211    IN                A                     142.250.10.100
DNS           TTl    internet class    type of record(ipv4)  returned ipv4 address

# What is an IPv4 address? How is it structured? 
- IPv4 is 32-bit numeric address
- Written in dotted decimal for humans
- Divided into octets
- Each device on a network must have a unique IPv4 address
- Network Portion – identifies the network the device belongs to
- Host Portion – identifies the specific device in that network
- The division depends on the subnet mask.
Example: 192.168.1.10/24 → first 24 bits (192.168.1) = network, last 8 bits = host.

# Difference between public and private IPs — give one example of each
Public IPs are the one whose end points can be accessed by anyone through internet 
- like Youtube anyone has internet can have accress
Private IPs are the one who can be accessed by the one who are of the same network or within that VPC
- like you are accessing the company portals

# What are the private IP ranges?
| Range                         | Subnet Mask       | Notes / Typical Use             |
| ----------------------------- | ----------------- | ------------------------------- |
| 10.0.0.0 – 10.255.255.255     | 255.0.0.0 (/8)    | Large networks, enterprise LANs |
| 172.16.0.0 – 172.31.255.255   | 255.240.0.0 (/12) | Medium-sized networks           |
| 192.168.0.0 – 192.168.255.255 | 255.255.0.0 (/16) | Home and small office networks  |.

# Run: ip addr show — identify which of your IPs are private

1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host noprefixroute
       valid_lft forever preferred_lft forever
2: ens5: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 9001 qdisc mq state UP group default qlen 1000
    link/ether 02:ec:b2:bd:ae:d7 brd ff:ff:ff:ff:ff:ff
    altname enp0s5
    altname eni-0faadc47c7b255505
    altname device-number-0.0
    inet 172.31.33.183/20 metric 512 brd 172.31.47.255 scope global dynamic ens5
       valid_lft 3558sec preferred_lft 3558sec
    inet6 fe80::ec:b2ff:febd:aed7/64 scope link proto kernel_ll
       valid_lft forever preferred_lft forever analyse this 
       
| Interface | IPv4 Address     | Private/Public     | Notes                                                        |
| --------- | ---------------- | ------------------ | ------------------------------------------------------------ |
| lo        | 127.0.0.1/8      | Private (loopback) | Internal testing only                                        |
| ens5      | 172.31.33.183/20 | Private            | LAN/VPC interface, cannot be accessed directly from Internet |

| Interface | IPv6 Address               | Scope      |
| --------- | -------------------------- | ---------- |
| lo        | ::1/128                    | Host-only  |
| ens5      | fe80::ec:b2ff:febd:aed7/64 | Link-local |


# What does /24 mean in 192.168.1.0/24?
total bits are 32 but here 24 bits are fixed 32 - 24 = 8 2^8 bits is obtained but 2^8 - 2 = total usable hosts 

# How many usable hosts in a /24? A /16? A /28?
32 - 24 = 8 == 2^8 - 2 = total usable bits 
32 - 16 = 16 == 2^16 - 2 =  total usable bits 
32 - 28 = 4 == 2^4 -2 =  total usable bits 

# Explain in your own words: why do we subnet?
to segregate the whole network into small networks so the we can use that for a isolation and access restriction 

| CIDR | Subnet Mask     | Total IPs    | Usable Hosts        |
| ---- | --------------- | ------------ | ------------------- |
| /24  | 255.255.255.0   | 2⁸ = 256     | 256 − 2 = 254       |
| /16  | 255.255.0.0     | 2¹⁶ = 65,536 | 65,536 − 2 = 65,534 |
| /28  | 255.255.255.240 | 2⁴ = 16      | 16 − 2 = 14         |

# What is a port? Why do we need them?
ports are the logical enpoints where the networking protocals will interact 
Port	Service
22	- SSh
80	- http
443	- https
53	- DNS
3306	- dtatbase/mysql/arora
6379	- Redis in-memory database
27017	- MongoDB database server

# You run curl http://myapp.com:8080 — what networking concepts from today are involved?
| Step | Concept Involved  | Explanation                                                            |
| ---- | ----------------- | ---------------------------------------------------------------------- |
| 1    | DNS Lookup        | `myapp.com` is resolved to an IP address using A/AAAA records.         |
| 2    | TCP Connection    | TCP handshake happens with the IP on **port 8080** (logical endpoint). |
| 3    | HTTP Request      | The HTTP protocol sends the request over the TCP connection.           |
| 4    | Routing & IP      | Packets travel over multiple routers/hops using the IP address.        |
| 5    | Application Layer | Your app server on port 8080 receives the request.                     |
| 6    | Response          | Server responds, packets follow back to your client.                   |

# Your app can't reach a database at 10.0.1.50:3306 — what would you check first?
- check whether the database port i,e 3306 is open or not
- then check whether we can ping to it
- check whether we are inside the CIDR or inside the VPC of the database where it is created
- Service Running-Ensure MySQL is actually running on the host and bound to 0.0.0.0 or the private IP





