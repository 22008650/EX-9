# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

## DATE :04-05-2023

## AIM :
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM :
1.Start the program.

2.Get the frame size from the user.

3.To create the frame based on the user request.

4.To send frames to server from the client side.

5.If your frames reach the server, it will send ACK signal to client otherwise it will sendNACK signal to client.

6.Stop the program

## PROGRAM :
## CLIENT:
## Developed : MALARVIZHI G
## Reg no : 212222040096

import socket

s=socket.socket()

s.connect(('localhost',8000))

while True:

    msg=input("Client > ")
    
    s.send(msg.encode())
    
    print("Server > ",s.recv(1024).decode())
    
## SERVER:
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



## OUTPUT :
## CLIENT:
![EX 9 CLIENT](https://github.com/22008650/EX-9/assets/122548204/0fe0941d-7a63-4b9f-970d-b82fd81e9622)
## SERVER:
![EX 9 SERVER](https://github.com/22008650/EX-9/assets/122548204/2f1c3faa-2d48-477d-b8d3-8845d31f71e6)




## RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
