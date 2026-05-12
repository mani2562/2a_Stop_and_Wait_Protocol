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
s.bind(('localhost',8080))
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
<img width="838" height="1005" alt="Screenshot 2026-05-12 101323" src="https://github.com/user-attachments/assets/0a893f47-e755-498b-bd5e-b8987ee674ad" />
<img width="854" height="993" alt="Screenshot 2026-05-12 101337" src="https://github.com/user-attachments/assets/5b42dd0c-76c5-4429-a843-c072d3fce604" />

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
