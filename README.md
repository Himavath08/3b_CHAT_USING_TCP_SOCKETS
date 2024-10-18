# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
# client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
# server
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

## OUPUT
# client
![Screenshot 2024-10-18 154055](https://github.com/user-attachments/assets/18799839-0cf3-4d4f-a442-b1cbdbdaf702)
# server
![Screenshot 2024-10-18 154104](https://github.com/user-attachments/assets/f24a7d3b-8fcd-4d2e-861a-2dedafdc6d21)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
