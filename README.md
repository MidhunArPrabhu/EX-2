# EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL

## DATE: 

## AIM :
To write a python program to perform sliding window protocol


## ALGORITHM : 
- Start the program.
- Get the frame size from the user
- To create the frame based on the user request.
- To send frames to server from the client side.
- If your frames reach the server it will send ACK signal to client otherwise it will sendNACK signal to client.

- Stop the program

## CLIENT PROGRAM :
```PYTHON 3 
## Developed : MIDHUN AZHAHU RAJA P
## Reg no : 212222240066
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
 print(ack)
 continue
 else:
 c.close()
 break
```
## SERVER PROGRAM :
```PYTHON 3
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
```


## OUTPUT :

![EX 2](https://github.com/MidhunArPrabhu/EX-2/assets/118054670/8c4a6091-7911-46ab-be85-d22341fb14b1)


## RESULT :

Thus, python program to perform stop and wait protocol was successfully executed.



