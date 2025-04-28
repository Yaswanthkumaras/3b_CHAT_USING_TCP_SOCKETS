# 3b.CREATION FOR CHAT USING TCP SOCKETS
### NAME:RAJAMANIKANDAN R
### REG NO:212223220082
# AIM
To write a python program for creating Chat using TCP Sockets Links.
# ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
# PROGRAM
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
# OUTPUT:
## CLIENT:
![322514815-3b201be5-286e-4c0c-8850-196d6fc63d19](https://github.com/rajamanikandanravikumar/3b_CHAT_USING_TCP_SOCKETS/assets/145742839/859c9047-79f8-4173-8415-7e09c238c26a)
## SERVER
![322514861-0adf18e4-39c9-47c3-ab12-b565672b312d](https://github.com/rajamanikandanravikumar/3b_CHAT_USING_TCP_SOCKETS/assets/145742839/7c2d13ce-8eb7-48b6-9e5f-77b3d0f920ad)

# RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
