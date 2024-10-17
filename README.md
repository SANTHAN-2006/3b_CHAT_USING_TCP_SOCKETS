# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.

## PROGRAM :

## Client.py :

```python
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```

## OUPUT :

![image](https://github.com/user-attachments/assets/5c5a79b3-2cca-4eb3-9707-8d87ce3bc3df)

## Server.py :

```python
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

## Output :

![image](https://github.com/user-attachments/assets/1cc0bd1a-760f-4dab-bf5b-d9867a17b453)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
