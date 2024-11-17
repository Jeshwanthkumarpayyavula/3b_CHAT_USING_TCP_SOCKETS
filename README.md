# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Name : P Jeshwanth Kumar
## Register number : 212223240114
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## Client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client>")
 s.send(msg.encode())
 print("Server>",s.recv(1024).decode())
```
## Server
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client>",ClientMessage)
 msg=input("Server>")
 c.send(msg.encode())
```

## OUPUT
## Client
![image](https://github.com/user-attachments/assets/3a2b7acd-df67-444d-806d-4495a809be8e)

## Server
![image](https://github.com/user-attachments/assets/8eccbc06-7914-4ffc-881d-519b765122ff)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
