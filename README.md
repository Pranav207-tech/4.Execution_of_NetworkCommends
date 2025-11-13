# EXECUTION OF NETWORK COMMENDS
## Name : Pranav K
## Reg no: 212224040240
## AIM :
Use of Network commands in Real Time environment
## Software : 
Command Prompt And Network Protocol Analyzer
## Procedure: 
### To do this EXPERIMENT- follows these steps:

1. In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
2. All commands related to Network configuration which includes how to switch to privilege mode and normal mode and how to configure router interface and how to save this configuration to flash memory or permanent memory.

  This commands includes

    • Configuring the Router commands
    • General Commands to configure network
    • Privileged Mode commands of a router 
    • Router Processes & Statistics
    • IP Commands
    • Other IP Commands e.g. show ip route etc.

## Program
### Client
```
.py
import socket
from pythonping import ping
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    hostname=c.recv(1024).decode()
    try:
        c.send(str(ping(hostname, verbose=False)).encode())
    except Exception as e:  # Catch all errors
        c.send(f"Error: {str(e)}".encode())

```
### Server
```
.py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    ip=input("Enter the website you want to ping ")
    s.send(ip.encode())
    print(s.recv(1024).decode())
```


## Output
### Client
<img width="572" height="197" alt="image" src="https://github.com/user-attachments/assets/8534dd41-c003-4c84-a41a-51b3eb9878f5" />

### Server
<img width="591" height="183" alt="image" src="https://github.com/user-attachments/assets/11455d37-2a3f-4fb5-baa3-7d271c1188f6" />

## netstat
<img width="1682" height="752" alt="Screenshot 2025-11-12 114658" src="https://github.com/user-attachments/assets/7701ff13-9c38-4d1c-ac22-a8daf9712f24" />

## ipconfig
<img width="1511" height="780" alt="Screenshot 2025-11-12 114339" src="https://github.com/user-attachments/assets/87aa7f2a-97b2-4b02-8f9e-25c5ab2b7721" />

## ping 
<img width="1709" height="742" alt="Screenshot 2025-11-12 114716" src="https://github.com/user-attachments/assets/d23c81c4-ee05-400b-a6b1-2f95a9a702b6" />

## tracert
<img width="1738" height="320" alt="Screenshot 2025-11-12 114738" src="https://github.com/user-attachments/assets/cbd4a403-a041-491b-9dfb-2708d09b52f2" />

## nslookup
<img width="1694" height="274" alt="Screenshot 2025-11-12 114752" src="https://github.com/user-attachments/assets/d812b365-953b-4388-9ccc-73bab49ea67e" />

## getmac
<img width="1653" height="168" alt="Screenshot 2025-11-12 114804" src="https://github.com/user-attachments/assets/cb23570a-afa7-402c-b189-0daf01f76074" />

## hostname
<img width="1810" height="56" alt="Screenshot 2025-11-12 114823" src="https://github.com/user-attachments/assets/4340a577-f197-407d-8ee6-a84b67511f2a" />

## nbtstat
<img width="1323" height="574" alt="Screenshot 2025-11-12 114835" src="https://github.com/user-attachments/assets/d884313f-ad18-4bb3-b324-30355115250d" />

## arp
<img width="1752" height="729" alt="Screenshot 2025-11-12 114855" src="https://github.com/user-attachments/assets/55bf4975-802e-46cb-84c1-b5ca89748179" />

## systeminfo
<img width="1601" height="768" alt="Screenshot 2025-11-12 114923" src="https://github.com/user-attachments/assets/2f9b4526-6a11-4fa1-9f4e-f448a9b9b72f" />


## Result
Thus Execution of Network commands Performed
