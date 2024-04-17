# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## ALGORITHM:
<BR>
Step 1: start the program.
<BR>
Step 2: Include necessary package in java.
<BR>
Step 3: To create a process object p to implement the ping command.
<BR>
Step 4: declare one Buffered Reader stream class object.
<BR>
Step 5: Get the details of the server
<BR>
 5:1: length of the IP address.
 <BR>
 5:2: time required to get the details.
 <BR>
 5:3: send packets, receive packets and lost packets.
 <BR>
 5.4: minimum, maximum and average times.
 <BR>
Step 6: print the results.
<BR>
Step 7: Stop the program.
<BR>

## Program:
**CLIENT:**
```
import socket
from pythonping import ping
s=socket.socket()
s.bind(('localhost'8000))
s.listen(5)
c,addr=s.accept()
while True:
 hostname=c.recv(1024).decode()
 try:
 c.send(str(ping(hostname, verbose=False)).encode())
 except KeyError:
 c.send("Not Found".encode())
```
**SERVER:**
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 ip=input("Enter the website you want to ping ")
 s.send(ip.encode())
 print(s.recv(1024).decode())
```
### Output:
## CLIENT:
![image](https://github.com/kaviya546/4.Execution_of_NetworkCommends/assets/150368823/fc4d4e30-9ec6-407d-9987-1e61b1e1baa6)

## SERVER:
![image](https://github.com/kaviya546/4.Execution_of_NetworkCommends/assets/150368823/7bf9e880-31ca-4a24-98b6-b756c1b42ff3)



## Result
Thus Execution of Network commands Performed.

# 4(b).WRITE A CODE SIMULATING TRACEROUTE COMMAND

## DATE:
## AIM:To write the python program for simulating Traceroute command
## ALGORITHM:
<BR>
1. Start the program.
<BR>
2. Get the frame size from the user.
<BR>
3. To create the frame based on the user request.
<BR>
4. To send frames to server from the client side.
<BR>
5. If your frames reach the server, it will send ACK signal to client
otherwise it will sendNACK signal to client.
<BR>
6. Stop the program
<BR>

## PROGRAM:
```
from scapy.all import*
target = ["www.google.com"]
result, unans = traceroute(target,maxttl=32)
print(result,unans)
```
### OUTPUT:

![image](https://github.com/kaviya546/4.Execution_of_NetworkCommends/assets/150368823/30d5ffe3-9fb4-415a-97ee-3543bf5a2930)



## Result
Thus Execution of Network commands Performed 
