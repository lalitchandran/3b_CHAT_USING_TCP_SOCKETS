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

## server:
```
 
import socket 
s=socket.socket() 
s.bind(('localhost',8080)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```
## client:
```
 
import socket 
s=socket.socket() 
s.connect(('localhost',8080)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode()) 
```
## OUPUT
# server:
![image](https://github.com/AasrithSairam/3b_CHAT_USING_TCP_SOCKETS/assets/139331438/ba4a2c39-d034-4093-88e6-ac11c5991f40)
# client:
![image](https://github.com/AasrithSairam/3b_CHAT_USING_TCP_SOCKETS/assets/139331438/6538fc0f-5d41-4f9b-9998-4e368d8176c2)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.



## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
