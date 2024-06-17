

#### SMB
SMB - Server Message Block - request-response protocol 
works on tcp/ip suite actually netbios over tcp/ip

enum4linux is a tool for enumerating smb shares both on windows and linux systems
wrapper around tools in samba and make it easy to quickly extract information 


Learn More About SMB


### Telnet 
application protocol  -connect and execute command on a remote machine

not secure - lacks encryption - slowly replace by ssh


### FTP 
file transfer protocol 
21 - command channel
20 - data channel 


- In an Active FTP connection, the client opens a port and listens. The server is required to actively connect to it. 
- In a Passive FTP connection, the server opens a port and listens (passively) and the client connects to it.



### NFS

Network File System : allows a system to share directory or files over network 

uses rpc to connect client and server

Understand NFS how to it was exploited


### SMTP

Simple mail transfer protocol -> sending of emails 

smtp performs 3 basic functions
- verifies who send the email
- sends the outgoing mail
- if the outgoing mail cant be delivered it sends the message back to the sender

### POP and IMAP