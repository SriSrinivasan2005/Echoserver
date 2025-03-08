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
Server side:

import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
```
```
client side:

import socket
HOST, PORT = '127.0.0.1', 65432
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as client:
    client.connect((HOST, PORT))
    client.sendall(b'srinivasan K ,24900578')

    response = client.recv(1024)
    print(f"Server says: {response.decode()}")
```
## OUTPUT:
Server side:
![alt text](<Screenshot 2025-03-08 140057.png>)

Client side:
![alt text](<Screenshot 2025-03-08 140134.png>)

## RESULT:
The program is executed successfully
