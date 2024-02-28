# 2a_Stop_and_Wait_Protocol

## AIM 
To write a python program to perform stop and wait protocol

## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program

## PROGRAM
```
import socket
s=socket.socket()
s.bind(('localhost', 8000))
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
## OUTPUT
```
Client Output
```
![image](https://github.com/SivaramakrishnanBaskar/2a_Stop_and_Wait_Protocol/assets/119476322/3d8a4ecd-79d4-474e-96bc-ae2bc678a982)

```
Server Output
```
![image](https://github.com/SivaramakrishnanBaskar/2a_Stop_and_Wait_Protocol/assets/119476322/687c4c4d-a310-4511-8c02-7b3f8c906e38)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
