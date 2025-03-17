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
# Client Side:
```python
import socket
HOST = "127.0.0.1"  
PORT = 65432  
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Hello, world")
    data = s.recv(1024)
print(f"Received {data!r}")

```

# Server Side:
```python
import socket
HOST = "127.0.0.1"  
PORT = 65432  
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while  data := conn.recv(1024):
            conn.sendall(data)

```
## OUTPUT:
![image](https://github.com/user-attachments/assets/d5592b8b-4b78-4001-a264-a2ffb21475c6)


## RESULT:
The program is executed successfully
