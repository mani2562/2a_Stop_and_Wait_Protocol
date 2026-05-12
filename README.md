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
## client
~~~
import socket
s=socket.socket()
s.connect(('localhost',8080))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Received ".encode())
import socket
s=socket.socket()
s.connect(('localhost',8080))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Received ".encode())

~~~
## server
~~~
import socket
s=socket.socket()
s.connect(('localhost',8080))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Received ".encode())
~~~
## OUTPUT
<img width="838" height="1005" alt="Screenshot 2026-05-12 101323" src="https://github.com/user-attachments/assets/72c6f1a1-c6a7-465a-9c58-2ce0898e05ac" />

<img width="854" height="993" alt="Screenshot 2026-05-12 101337" src="https://github.com/user-attachments/assets/ae78f9f4-c1b3-4090-a016-f6216c34fbf0" />

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
