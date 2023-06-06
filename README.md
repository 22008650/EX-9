# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

## DATE :04-05-2023

## AIM :
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM :
### STEP 1: Start the program.
### STEP 2: Get the frame size from the user.
### STEP 3: To create the frame based on the user request.
### STEP 4: To send frames to server from the client side.
### STEP 5: If your frames reach the server, it will send ACK signal to client otherwise it will sendNACK signal to client.
### STEP 6: Stop the program

## PROGRAM :
## CLIENT:
## Developed : MALARVIZHI G
## Reg no : 212222040096
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


## OUTPUT :
## CLIENT:
![ex09 client output](https://github.com/22008650/EX-9/assets/122548204/652ed6f7-90c6-4733-b461-4915ec84174c)
## SERVER:
![ex09 server output](https://github.com/22008650/EX-9/assets/122548204/6d413bb2-6e06-4c95-9738-caac6623d8a9)





## RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
