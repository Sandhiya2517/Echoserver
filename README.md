# Echoserver
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
    s.sendall(b'Sandhiya M, 212224220086')
    print(f'Received: {s.recv(1024)!r}')

```


## OUTPUT:
![Screenshot 2025-03-03 140744](https://github.com/user-attachments/assets/023d2aca-a7c8-4e68-8c5c-2a3ca5a96889)

![Screenshot 2025-03-03 140734](https://github.com/user-attachments/assets/41715504-ac34-4e00-8767-370817c83a43)


## RESULT:
The program is executed successfully
