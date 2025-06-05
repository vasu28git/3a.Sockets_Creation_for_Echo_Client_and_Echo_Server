# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
1.Client:
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
2.server:
```python
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## OUTPUT:
1.CLIENT:
![image](https://github.com/user-attachments/assets/23ed9ac6-3fbe-4384-a1fd-42bb4114a58d)
2.SERVER:
![image](https://github.com/user-attachments/assets/b74818a5-55fd-44c6-aed7-becf802735c5)
## RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
