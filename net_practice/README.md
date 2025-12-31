<h1 align="center">🌐 NetPractice – Networking Fundamentals</h1>
<p align="center">
  <b>A beginner-friendly guide to IP, TCP, TCP/IP, and the OSI Model</b><br/>
  🚀 Understand the core protocols that power the Internet
</p>

---
      
## 📍 1. IP (Internet Protocol)
**What it is:**  
The protocol that defines how devices **identify** and **locate** each other on a network, and how data packets are delivered.

### 📍 Get Your Ip in MacOS Or windows:
```c
	curl ifconfig.me
	\\ OR
	ipconfig
```

- **Main role:** Addressing & Routing  
- **Analogy:** Like a **street address** for your home – tells the postman where to deliver letters.  

### 🌍 Versions of IP
| Feature     | IPv4 (v4) | IPv6 (v6) |
|-------------|-----------|-----------|
| **Size**    | 32 bits (~4.3B addresses) | 128 bits (~340 undecillion addresses) |
| **Format**  | `192.168.1.10` (dotted decimal) | `2001:0db8:85a3::8a2e:0370:7334` (hex with colons) |
| **Problem** | Addresses running out | Virtually unlimited |
| **Extras**  | — | Built-in **IPsec**, efficient routing, auto-configuration |

#### 📍 Advantages over IPv6:
  - Much larger address space.
  - Built-in security features (IPsec).
  - More efficient routing.
  - Supports auto-configuration (devices can set their own IPs without DHCP).
---

## 📍 2. TCP (Transmission Control Protocol)

**What it is:**  
A protocol that ensures **reliable communication** between devices.

- **Main role:** Guarantees that data is delivered **completely and in order**.  
- **Analogy:** Like a **phone call** – you talk, the other person says *"Got it!"*.

✅ TCP handles:  
- 📦 Splitting data into packets  
- 🔢 Numbering packets  
- ✅ Error checking  
- 🔄 Resending lost packets  
- 🏗 Reassembling packets  

---

## 📍 3. TCP/IP (The Internet Foundation)

**What it is:**  
The combination of **TCP + IP** protocols = the foundation of the Internet.  

- 🌍 **IP** → Decides *where* data goes  
- 📞 **TCP** → Ensures *how* data arrives  

 > Data Flow:
	\- Data → TCP (split/check) → IP (address/route) → Internet → TCP (rebuild) → App
---

## 📍 4. TCP/IP Addresses

A **TCP/IP address** usually refers to an **IP address**, but real communication also requires a **port**.  
   *IP Address: The location (e.g., 192.168.1.5)*
   *Port Number (TCP/UDP): The specific service (e.g., port 80 for web, 22 for SSH)*

 🌐 IP + Port Example
   Example: `192.168.1.5:80`
   - `192.168.1.5` → Device **IP Address**  
   - `:80` → **Service Port** (Web server)

## 🎯 Understanding Ports (0 – 65535)

🔹 **What are Ports?**  
Ports are **logical endpoints** that allow multiple services to run on the **same device**.  
They make sure your computer knows **which application** should handle incoming data.  

📦 **Example:**  
- 🌐 Web servers → **Port 80 (HTTP)** & **Port 443 (HTTPS)**  
- 📧 Email servers → **Port 25 (SMTP)**  
- 🎮 Games & apps → use different custom ports  

➡️ Thanks to ports, your computer can run **multiple networked services simultaneously**, and still deliver the right data to the right program.  

---

### 🔹 Port Ranges

| Range              | Type             | Use Case |
|--------------------|-----------------|----------|
| **0 – 1023**       | **Well-Known Ports** | Reserved for core services (HTTP, HTTPS, FTP, SSH) |
| **1024 – 49151**   | **Registered Ports** | Used by user applications & processes |
| **49152 – 65535**  | **Dynamic / Private Ports** | Temporary (ephemeral) ports chosen automatically |

---

### 📖 Quick Example
When you visit `https://example.com`:  
1. Your browser connects to the server’s **IP address**.  
2. It specifically requests data from **Port 443** (HTTPS).  
3. The server listens on Port 443 → responds with the website content.  

✅ Client (Your PC) → 93.184.216.34:443 (Server HTTPS Port)
 	-> Without ports, all data would arrive in one place with no way to separate web traffic, email, games, etc.

---

### 📦 Common Web Server Ports
- **Port 80** →  (insecure web traffic)
- **Port 443** → (secure web traffic with TLS/SSL)

---

### 🔹 Establishing Connections
When your browser connects to a website:
1. It looks up the server’s **IP address** (via DNS).  
2. It connects to the server on a specific **port**.  
   - Port **80** → Uses **HTTP** (Hypertext Transfer Protocol). HTTP (insecure web traffic)
   - Port **443** → Uses **HTTPS** (HTTP Secure, encrypted with TLS/SSL). HTTPS (secure web traffic with TLS/SSL)

## ✅ Summary:
  - 🌍 **IP** = Address system (where /Addressing/).
  - 📞 **TCP** = Reliable transport (how).
  - ⚡ **TCP/IP** = Core Internet protocols \ that powers the Internet.
  - 🏠 **TCP/IP Address** = [IP + Port] Usually just an IP address used with TCP.
  
---

## 🌐 Example: Visiting a Website

1️⃣ **DNS Resolution**  
- Your PC asks DNS: *"What is the IP of example.com?"*  
- DNS replies: `93.184.216.34`

2️⃣ **TCP Connection Setup (3-Way Handshake)**  
PC → SYN → Server
Server → SYN-ACK → PC
PC → ACK → Server
✅ Connection established  

---

## 📖 The OSI Model (7 Layers):

A **conceptual framework** for how systems communicate, created by ISO(International Organization for Standardization).  
    ✨ **Why it matters:**  
       \- 🧩 Standardization
       \- 🏗 Modularity 
       \- 🔗 Interoperability 
       \- 🪜 Layer Independence  
       \- 🔍 Easier Debugging 
       \- 📈 Scalability   
       \- 🎓 Education 
       \- 💡 Innovation  

### 🔹 7 Layers (Top → Bottom)

| # | Layer            | Role |
|---|-----------------|------|
| 07 | **Application**   | Closest to users – browsers, email, Zoom |
| 06 | **Presentation**  | Encryption, compression, encoding |
| 05 | **Session**       | Starts, manages, ends sessions |
| 04 | **Transport**     | Ensures delivery (TCP/UDP) |
| 03 | **Network**       | Addressing & routing (IP) |
| 02 | **Data Link**     | Local delivery (MAC, Ethernet/Wi-Fi) |
| 01 | **Physical**      | Signals, cables, connectors |

---

## 7️⃣ Application Layer (OSI Layer 7)

🔹 **What it is:**  
The Application Layer provides network services directly to end users.
It’s where applications like web browsers, email clients, and messaging apps interact with the network.  

---

### What the Application Layer Does
   - It provides the rules and services that applications use to communicate over the network.
   - Without it, your apps would have no standard way of “talking” to other computers.

✅ Example:
   - When you open a browser and type google.com:
   - Chrome itself is the application.  
   - But Chrome uses HTTP/HTTPS protocols (Application Layer) to ask Google’s servers for a webpage.
So, the Application Layer makes sure the browser and Google’s server understand each other.

**FOR WHAT: It exists so different apps on different systems can talk to each other**

✅ Example:
   - 🌍 Browsing → HTTP/HTTPS
   - 📧 Email → SMTP, IMAP, POP3
   - 🔍 Name resolution → DNS
   - 📂 File sharing → FTP, SMB 

### How It Works
   - Browser creates an **HTTP GET request** (**Application Layer**)
   - The application (browser, mail client, etc.) passes your request to the Application Layer.
   **The Application Layer:**    
   - Chooses the right protocol (HTTP, SMTP, DNS, etc.)
   - Structures the data so the other computer understands it.
   - It then sends the data down to the Presentation Layer → Transport Layer → Network → and out onto the internet.
   - On the other side, the receiver’s Application Layer interprets the request and delivers it to their app.
   \>**Basically → every time you “use the Internet,” you’re triggering the Application Layer.**

---

## 🎭 Presentation Layer (OSI Layer 6)

🔹 **What it is:**  
The Presentation Layer acts as the **translator** of the OSI model.  
It ensures that the data sent by the Application Layer of one system can be **read, formatted, compressed, or encrypted** so the receiving system can understand it.  

---

### 🛠 Main Responsibilities
- 🔡 **Translation / Encoding** → Converts data formats so both sides understand (e.g., ASCII ↔ UTF-8).  
- 📦 **Compression** → Reduces data size to save bandwidth (e.g.ZIP, GIF, JPEG, MP3, MPEG) **File Formats:**. 
- 🔒 **Encryption / Decryption** → Secures data before transmission (e.g., SSL/TLS for HTTPS).  
 🔹 TLS/SSL Handshake (Simplified)

   ```C
      Client                                    Server
      ------                                    ------
         |  SYN  ------------------------------   |
         |       ----------------------> SYN_ACK  |
         |  ACK  <-----------------------------   |	+-------------------------------------------------------------------------------+
         | SYN → SYN-ACK → ACK (TCP C establish)  |	|	📦 Examples in Real Life	                                                  |
         |  ClientHello ----------------------->  |	|		File Formats: JPEG, PNG, MP3, MP4, PDF → standard presentation formats.   |
         |                                        |	|		Data Encoding: ASCII, UTF-8, EBCDIC.								              |				
         |  <----------------- Server Hello/i get |	|		Encryption: SSL/TLS (used in HTTPS).									           |				
         |  <------------------- Certificate      |	|		Compression: ZIP, GIF, MPEG.									               	  |		
         |  <----------------- Server_Hello_Done  |	+-------------------------------------------------------------------------------+
         |                                        |
         | Client_Key_Exchange ---------------->  |  ChangeCipherSpec ||<<
         |  ChangeCipherSpec ------------------>  |  يتحول كلا الجانبين إلى الوضع المشفر.
         |  Finished -------------------------->  |
         |                                        |
         |  <----------------- ChangeCipherSpec   |
         |  <------------------- Finished         |
   ```

---

### 📚 Example Flow (HTTPS Request)
1. Browser creates an **HTTP request** (Application Layer).  
2. **Presentation Layer**:  
   - 🔒 Encrypts with TLS/SSL  
   - 🔡 Encodes text in : ASCII, UTF-8, EBCDIC   
   - 📦 Compresses data if needed → ZIP, GIF, MPEG
3. Transport Layer (TCP) ensures delivery.  
4. Network Layer (IP) routes the packets.  

---

### ✅ Key Takeaways
- 📌 **Goal:** Make data **readable, secure, and efficient**.  
- ⚡ Services provided: **Translation, Compression, Encryption**.  
- 🧑‍💻 Users don’t see it directly, but it works behind the scenes every time you browse securely, stream, or share files.  

---

## 5️⃣ 🗨️ Session Layer

📍 **What it is:**  
   The **Session Layer** manages and controls the **dialog (sessions)** between two devices. 
   it’s a manager that sits on top of TCP to control the conversation.
   It decides **who talks, when, and for how long**.  
👉 **Analogy:** Like a **moderator in a meeting**, keeping conversations orderly.  

- Without it → chaos: overlapping talk, broken logins, no crash recovery.  

---

### 🛠 Main Responsibilities
- 🔗 **Establishing Sessions**  
   - Starts communication between devices.  
   - Example: Logging into a server via SSH.  

- 🔄 **Maintaining Sessions**  
   - Keeps ongoing connections alive.  
   - Example: A video call staying active.  

- ⏱ **Synchronizing**  
   - Adds **checkpoints** in long transmissions so recovery is possible.  
   - Example: Resume a download from 1.5GB instead of restarting a 2GB file.  

- 🛑 **Terminating Sessions**  
   - Gracefully ends communication when finished.  
   - Example: Clicking **Log Out** closes the session.  

---

### 📦 Real-Life Examples

   1. Your computer and the server agree: “We can talk. The road is open.” (that’s the TCP handshake).
   2. Session Layer jumps: 

      It says: “Okay, before we start, let’s set the rules:
         - Who’s the client (you) and who’s the server.
         - What language/security to use (password, encryption, etc.).
         - How long this talk will last before timeout.”
   3. Session Layer jumps in
      - It says: “Okay, before we start, let’s set the rules:
      - Who’s the client (you) and who’s the server.
      - What language/security to use (password, encryption, etc.).
      - How long this talk will last before timeout.”
   4. Authentication happens
      - Server: “Who are you?”
      - You: “I’m user123, here’s my password/key.”
      - Server: “Okay, you’re in. Session established.”
   5. Conversation is managed
      - Every command you type in SSH now goes through that session.
      - If the connection blips, checkpoints let you resume without starting from zero.
   6. Ending the session
      - You type exit.
      - Session Layer: “Conversation is over, close it cleanly.”
      - TCP: removes the road.

---

## 🚚 Transport Layer (OSI Layer 4)

🔹 **What it is:**  
The Transport Layer is responsible for the **end-to-end delivery of data** between applications on different devices.  
It makes sure data is delivered **reliably, in the correct order, and without errors** (if needed).  

---

### 🛠 Main Responsibilities
- **Multiplex/Demultiplex**
by ports (many apps share one IP)
- 📦 **Segmentation & Reassembly**  
  Breaks large messages into smaller chunks (segments) and reassembles them at the destination.  

- ✅ **Error Detection & Correction**  
  Ensures data arrives intact; retransmits if necessary.  

- 🔢 **Ordering**  
  Keeps track of sequence numbers so packets arrive in the correct order.  

- 🎯 **Multiplexing with Ports**  
  Uses **port numbers** (0–65535) to deliver data to the right application.  
  Example: Port 80 → Web server, Port 22 → SSH.  

- ⚡ **Flow Control**  
  Prevents one device from overwhelming another by sending too much data at once.  

---

### 🔑 Core jobs:

- Multiplex/Demultiplex by ports (many apps share one IP)

- Segmentation/Reassembly (break big messages into MSS-sized segments)
- Reliability & Ordering (TCP) or low overhead (UDP)
- Flow Control (don’t overrun the receiver)
- Congestion Control (don’t flood the network)

---
























+-------------------------------------------------------------+
|                 Application Layer (Layer 7)                 |
|  - Programs users interact with (Browser, Zoom, Email)       |
|  - Generates requests (HTTP GET, SQL query, Chat message)    |
|  - Example: "GET /index.html" or "ssh user@server"          |
+-------------------------------------------------------------+
                              │
                              ▼
+-------------------------------------------------------------+
|                Presentation Layer (Layer 6)                 |
|  - Translates data formats (JSON, XML, HTML, JPEG, MP3)      |
|  - Handles encryption (TLS/SSL, AES)                        |
|  - Handles compression (gzip, video codecs)                 |
|  - Example: HTTPS encrypts your HTTP request before sending  |
+-------------------------------------------------------------+
                              │
                              ▼
+-------------------------------------------------------------+
|                   Session Layer (Layer 5)                   |
|  - Manages dialogs: establishes, maintains, terminates       |
|  - Authenticates users (login sessions, tokens, keys)        |
|  - Synchronization (checkpoints in file transfer/streaming)  |
|  - Example: SSH login, SQL session, Zoom call state mgmt     |
+-------------------------------------------------------------+
                              │
                              ▼
+-------------------------------------------------------------+
|                 Transport Layer (Layer 4)                   |
|  - Ensures reliable delivery (TCP) or fast delivery (UDP)    |
|  - Breaks data into segments & reassembles on other side     |
|  - Provides ports (80=HTTP, 443=HTTPS, 22=SSH, 25=SMTP)      |
|  - Example: TCP 3-way handshake (SYN → SYN-ACK → ACK)        |
+-------------------------------------------------------------+
                              │
                              ▼
             (then continues to Network, Data Link, Physical)

<p align="center">
  Made with ❤️ for learning and practicing <b>Networking Fundamentals</b>
</p>
∆


















































# NetPractice Complete Guide

## Table of Contents
1. IP Addressing Fundamentals
2. Subnet Masks & CIDR Notation
3. Network Classes and Private IPs
4. Routing Concepts
5. Practical Problem-Solving Strategy

---

## 1. IP Addressing Fundamentals

### What is an IP Address?
An IP address is a 32-bit number written as four octets (bytes) separated by dots.

**Example:** `192.168.1.1`
- Binary: `11000000.10101000.00000001.00000001`
- Each octet ranges from 0 to 255

### Structure of an IP Address
Every IP address has two parts:
- **Network portion**: Identifies the network
- **Host portion**: Identifies the device on that network

The subnet mask determines where the split occurs.

---

## 2. Subnet Masks & CIDR Notation

### What is a Subnet Mask?
A subnet mask separates the network and host portions of an IP address.

**Common Subnet Masks:**
```
255.255.255.0   = /24  (254 usable hosts)
255.255.255.128 = /25  (126 usable hosts)
255.255.255.192 = /26  (62 usable hosts)
255.255.255.224 = /27  (30 usable hosts)
255.255.255.240 = /28  (14 usable hosts)
255.255.255.248 = /29  (6 usable hosts)
255.255.255.252 = /30  (2 usable hosts) - Perfect for point-to-point links
255.255.0.0     = /16  (65,534 usable hosts)
255.0.0.0       = /8   (16,777,214 usable hosts)
```

### CIDR Notation Explained
The `/24` notation tells you how many bits are used for the network portion.

**Example: 192.168.1.0/24**
- `/24` means the first 24 bits are the network
- Remaining 8 bits are for hosts
- Network: `192.168.1.0`
- Usable IPs: `192.168.1.1` to `192.168.1.254`
- Broadcast: `192.168.1.255`

### Calculating Subnets

**Formula for usable hosts:**
```
Usable Hosts = 2^(32 - prefix) - 2
```

**Example with /30:**
- 2^(32-30) - 2 = 2^2 - 2 = 4 - 2 = 2 usable hosts
- Perfect for router-to-router connections

**Example with /26:**
- 2^(32-26) - 2 = 2^6 - 2 = 64 - 2 = 62 usable hosts

### Finding Network Address
To find which network an IP belongs to, perform a bitwise AND between the IP and subnet mask.

**Example:**
```
IP:    192.168.1.130
Mask:  255.255.255.192 (/26)

Binary AND operation:
11000000.10101000.00000001.10000010  (IP)
11111111.11111111.11111111.11000000  (Mask)
-----------------------------------
11000000.10101000.00000001.10000000  = 192.168.1.128

Network: 192.168.1.128/26
Range:   192.168.1.129 - 192.168.1.190 (usable)
Broadcast: 192.168.1.191
```

---

## 3. Network Classes and Private IPs

### Private IP Ranges (RFC 1918)
These are reserved for internal networks and NOT routable on the internet:

```
Class A: 10.0.0.0        - 10.255.255.255   (/8)
Class B: 172.16.0.0      - 172.31.255.255   (/12)
Class C: 192.168.0.0     - 192.168.255.255  (/16)
```

### Special Addresses
```
127.0.0.0/8      - Loopback (localhost)
0.0.0.0          - Default route
255.255.255.255  - Broadcast to all
```

---

## 4. Routing Concepts

### What is a Router?
A router connects different networks and forwards packets between them. Each router interface must be on a different network.

### Default Gateway
The default gateway is the IP address where a device sends traffic destined for other networks.

**Key Rule:** The gateway must be in the same network as the device.

**Example:**
```
Device:  192.168.1.10/24
Gateway: 192.168.1.1     ✓ (same network)
Gateway: 192.168.2.1     ✗ (different network - won't work!)
```

### Routing Tables
Routers use routing tables to decide where to send packets.

**Routing Table Entry Components:**
- **Destination Network**: Where the packet is going
- **Next Hop**: The next router's IP to forward to
- **Default Route**: 0.0.0.0/0 (catch-all for unknown destinations)

**Example Routing Table:**
```
Destination       Next Hop        Interface
192.168.1.0/24    -               eth0 (directly connected)
10.0.0.0/8        192.168.1.254   eth0 (via gateway)
0.0.0.0/0         192.168.1.1     eth0 (default route)
```

---

## 5. Practical Problem-Solving Strategy

### Step 1: Identify the Network Topology
- How many networks are there?
- Which devices are on the same network?
- Where are the routers?

### Step 2: Assign IP Addresses
**Rules:**
1. Devices on the same switch/network must be in the same subnet
2. Each router interface must have a unique network
3. IP addresses in the same network must not overlap
4. Use appropriate subnet masks for the number of hosts

**Example:**
```
Network A (3 hosts): Use /29 (6 usable IPs)
Network B (50 hosts): Use /26 (62 usable IPs)
Router link: Use /30 (2 usable IPs)
```

### Step 3: Configure Subnet Masks
Both the IP address and subnet mask must match for devices to communicate.

**Common Mistake:**
```
Device A: 192.168.1.10/24
Device B: 192.168.1.20/25

These are in DIFFERENT networks! They can't communicate directly.
```

**Correct:**
```
Device A: 192.168.1.10/24
Device B: 192.168.1.20/24

Both in 192.168.1.0/24 - they can communicate!
```

### Step 4: Set Default Gateways
For devices that need to reach other networks:
- Gateway must be a router interface
- Gateway must be in the same network as the device

### Step 5: Configure Routing Tables
For routers to forward traffic:
- Add routes to destination networks
- Specify the next hop (another router's IP)
- Use default route (0.0.0.0/0) for internet access

### Step 6: Verify Connectivity
Check that:
- All devices in the same network can reach each other
- Devices can reach their gateway
- Routers can forward to destination networks
- Return path exists (routing is bidirectional!)

---

## Common NetPractice Scenarios

### Scenario 1: Simple LAN
```
[Computer A] --- [Switch] --- [Computer B]

Solution:
- Same network for both computers
- A: 192.168.1.10/24
- B: 192.168.1.20/24
```

### Scenario 2: Router Between Two Networks
```
[Network A] --- [Router] --- [Network B]

Solution:
- Network A: 192.168.1.0/24
  - Computer: 192.168.1.10/24
  - Router Interface: 192.168.1.1/24
  
- Network B: 192.168.2.0/24
  - Computer: 192.168.2.10/24
  - Router Interface: 192.168.2.1/24
  
- Gateway for Network A computers: 192.168.1.1
- Gateway for Network B computers: 192.168.2.1
```

### Scenario 3: Multiple Routers
```
[Net A] --- [Router1] --- [Router2] --- [Net B]

Solution:
- Network A: 10.0.1.0/24
- Link between routers: 10.0.2.0/30 (only 2 IPs needed)
- Network B: 10.0.3.0/24

Router1 needs route to Net B via Router2
Router2 needs route to Net A via Router1
```

---

## Quick Reference Cheat Sheet

### Subnet Mask Quick Reference
```
/30 = 255.255.255.252 → 2 hosts   (router links)
/29 = 255.255.255.248 → 6 hosts
/28 = 255.255.255.240 → 14 hosts
/27 = 255.255.255.224 → 30 hosts
/26 = 255.255.255.192 → 62 hosts
/25 = 255.255.255.128 → 126 hosts
/24 = 255.255.255.0   → 254 hosts (most common)
/16 = 255.255.0.0     → 65,534 hosts
/8  = 255.0.0.0       → 16,777,214 hosts
```

### Troubleshooting Checklist
- [ ] Are IPs in the same network using the same subnet mask?
- [ ] Is the gateway IP in the same network as the device?
- [ ] Are router interfaces on different networks?
- [ ] Do routing tables have entries for all destination networks?
- [ ] Is there a return path for traffic?
- [ ] Are there any IP conflicts (duplicate IPs)?

### Key Formulas
```
Number of hosts = 2^(32 - prefix) - 2
Network address = IP AND Subnet Mask
Broadcast = Network address + (Number of hosts + 1)
```

---

## Practice Tips

1. **Start Simple**: Master small networks before complex topologies
2. **Draw It Out**: Sketch the network to visualize connections
3. **Check Both Directions**: Traffic must flow both ways
4. **Use Consistent Subnets**: Keep subnet masks simple when possible
5. **Test Incrementally**: Use "Check again" frequently
6. **Read the Logs**: Error messages tell you exactly what's wrong

---

## Common Mistakes to Avoid

❌ Using overlapping IP ranges on different networks
❌ Setting gateway outside the device's network
❌ Forgetting to configure routing tables
❌ Using broadcast or network addresses for devices
❌ Mismatched subnet masks on the same network
❌ Router interfaces on the same network

✓ Each network has a unique range
✓ Gateway is always in the same subnet
✓ Routes point to the correct next hop
✓ Only usable IPs are assigned to devices
✓ All devices on a network share the same mask
✓ Each router interface is on a different network