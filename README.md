# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

## DATE:03-05-2023
## AIM:

To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
## Client:

Import the necessary modules in python Create a socket connection to using the socket module. Send message to the client and receive the message from the client using the Socket module in server Send and receive the message using the send function in socket.
## PROGRAM:
## CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
```
## SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
   ClientMessage=c.recv(1024).decode()
   print("Client > ",ClientMessage)
   msg=input("Server > ")
   c.send(msg.encode())
```
## CLIENT OUTPUT :
![241143134-7a1ae7c2-85c3-48f3-99ef-8e0cd8891521](https://github.com/Amruthavarshnibs/EX-9/assets/119103704/2320c0c4-eda6-4d59-b278-784c279a6087)


## SERVER OUTPUT :
![241143168-18d54810-4593-4b1a-ade7-889aae7943cb](https://github.com/Amruthavarshnibs/EX-9/assets/119103704/1e38cac0-0c5a-49eb-aaf4-552e5faba45e)


## RESULT:

Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
