<h1 align="center">🌐 NetPractice – Networking Fundamentals</h1>
<p align="center">
  <b>A beginner-friendly guide to IP, TCP, TCP/IP, and the OSI Model</b><br/>
  🚀 Understand the core protocols that power the Internet
</p>

---

## 📍 1. IP (Internet Protocol)
**What it is:**  
The protocol that defines how devices **identify** and **locate** each other on a network, and how data packets are delivered.

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


**TCP makes a road:**
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




| Technology | Usage |  
|------------|-------|
| **NetBIOS** | Basic session services |
| **RPC (Remote Procedure Call)** | Enables function calls over a network |
| **SQL Sessions** | Manage database connections |
| **API Sessions** | Authentication with tokens |
| **SSH / RDP** | Remote login & desktop sessions |


## 📚 Resources

- [RFC 791 – IP](https://www.rfc-editor.org/rfc/rfc791)  
- [RFC 793 – TCP](https://www.rfc-editor.org/rfc/rfc793)  
- [OSI Model – Wikipedia](https://en.wikipedia.org/wiki/OSI_model)  

---

<p align="center">
  Made with ❤️ for learning and practicing <b>Networking Fundamentals</b>
</p>
