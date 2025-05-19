#EX.1 Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
```
server.py
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)


client.py

import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'keerthika A, 212224220048')
    print(f'Received: {s.recv(1024)!r}')


```
## OUTPUT:

![Screenshot 2025-03-03 140114](https://github.com/user-attachments/assets/ef016a5e-cb1f-4548-a928-03cc30686b5a)

![Screenshot 2025-03-03 140132](https://github.com/user-attachments/assets/1af0777b-f712-4891-9863-d2a4760bded0)

## RESULT:
The program is executed successfully
