# Network-Monitoring-Tool

Project 1: Monitoring Tool for Lab Evaluations
The objective of this project is to develop a monitoring tool to stop copying during the lab
evaluations. Let us assume that there is a lab (for example, D313 at BITS) with 100 PCs. All
these PCs have USB connection, LAN connection and Internet connection. One PC is the
server and the rest 99 PCs are used by students.

## Write a tool that will do the following:

### 1. First, it will run at each PC and store all the logs of:
(i) if a student tries to do any
transfer using USB
(ii) if a student tries to do any transfer within a local network and
(iii) if a student tries to do any transfer using Internet.

### 2. The logs shall be first stored locally in each student PC. 
All the student PCs are connected with the server. Once the lab evaluation is completed, all these logs are
transferred to the server in the lab. The IP address of the server is fixed and known
by all the other PCs. Note that you may need to filter some traffic (for example ARP
packets or others) that are frequently traversing in the network and not related to
the copying.
## USBMonitor and PacketMonitor
> pyudev
> scapy
> Django (Server)

* Logs are stored only locally in the CLIENT_CODE Folder.
* SQLite is used to keep a track of all the connected Clients.
* Refer PDF for more.

In addition to the Step 2, your tool shall send the feedback from the student PC to
the server in real time. As soon as your tool at student PC detects copying from USB,
internal network or outside network, it shall notify this event to the server. The
notification message may contain the IP address of the client, the reference to the
log if it is regarding USB/internal-network/external-network copying, etc. Once you
receive this message at the server, you may display it as a real-time notification or
store it in a different file.
