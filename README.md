# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM :
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
## CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',9300))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',9300))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())
```
## OUTPUT:
## CLIENT:
![image](https://github.com/karthick-V-212223040086/3b_CHAT_USING_TCP_SOCKETS/assets/149037461/49d93a3d-b58a-4848-b6cf-c718230aa3c0)

## SERVER:
![image](https://github.com/karthick-V-212223040086/3b_CHAT_USING_TCP_SOCKETS/assets/149037461/2ce3a3b4-f734-47ae-ace4-dac025683f7c)
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
