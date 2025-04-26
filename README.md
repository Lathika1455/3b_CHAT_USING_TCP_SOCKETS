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
```import socket 
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
CLIENT

![cn 3b c](https://github.com/user-attachments/assets/7f9e92af-b76e-403e-a2fa-204ad8fcadcb)

SERVER

![cn 3b s](https://github.com/user-attachments/assets/6dacee0c-3fe1-47ff-b479-b062384336dc)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
