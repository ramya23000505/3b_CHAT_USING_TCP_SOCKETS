# 3b.CREATION FOR CHAT USING TCP SOCKETS
### Date:
### AIM
To write a python program for creating Chat using TCP Sockets Links.
### ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
### PROGRAM
#### Developed by: RAMYA R
#### Register by: 212223230169
### CLIENT
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
```
### SERVER
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
## OUTPUT
### CLIENT
![image](https://github.com/user-attachments/assets/93cd5b3d-4098-4893-bccd-e76331bddc4d)

### SERVER
![image](https://github.com/user-attachments/assets/a904a471-f118-4676-8bb2-6046440d1a23)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
