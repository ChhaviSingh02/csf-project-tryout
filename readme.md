Server-Client Communication Overview

Key Components:
1. Server:  Handles requests from the client, processes data, and sends responses.
2. Client:  Initiates requests and receives responses, typically a browser or application.
3. Addressing System:
   - Internet Service Provider (ISP): Exposes the IP address of connected devices and routes traffic.
   - IP Address (e.g., 192.13.13.1323): Identifies a specific device (like a street in a city).
   - Port Number: Differentiates services on the same device (like a house on the street).
   - Domain Name (e.g., www.dfg.com): A human-readable alias mapped to an IP address via DNS.

---
How Communication Happens:

1. Client Request Workflow:
   - The client sends a request to the server.
   - DNS (Domain Name System): Resolves the domain name to its corresponding IP address.
   - The connection is established using predefined rules (protocols).
   - Data is transferred back and forth between the client and the server.

2. Protocols:
   - HTTP (HyperText Transfer Protocol):** Used for web communication.
     - HTTP/1.0: Non-persistent (a new connection for every request/response).
     - HTTP/1.1: Persistent (single connection handles multiple requests/responses, widely used today).
   - TCP (Transmission Control Protocol):
     - Three-Way Handshake: Establishes a reliable connection.
       1. Client → Server: Sends a packet with `SYN` flag.
       2. Server → Client: Responds with `SYN + ACK` flags.
       3. Client → Server: Sends an `ACK` flag to confirm connection.
   - UDP (User Datagram Protocol): Enables direct, fast communication without connection establishment.
   - SMTP (Simple Mail Transfer Protocol): For sending emails.
   - FTP (File Transfer Protocol): For transferring files.

3. Sockets:
   - Socket API:Provides an interface for communication between the client and the server.
     - `socket.listen()`: Prepares the server to accept connections.
     - `socket.accept()`: Accepts incoming connections.
   - A single socket can handle multiple client threads.

---
Visual Representation of Workflow:

1.Basic Communication Flow:

   Client ---------------> DNS
                 IP <-----
                   |
                   |
                   |
                 Server

3. Request-Response Flow:
   
   Client ---- Request ----> Server
          <--- Response ---
   


     
     
     
        
         

  

  
  
