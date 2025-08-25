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

➡️ *Data Flow:*
	\- Data → TCP (split/check) → IP (address/route) → Internet → TCP (rebuild) → App
---

## 📍 4. TCP/IP Addresses

A **TCP/IP address** usually refers to an **IP address**, but real communication also requires a **port**.  

*IP Address: The location (e.g., 192.168.1.5)*
*Port Number (TCP/UDP): The specific service (e.g., port 80 for web, 22 for SSH)*
Example:  `192.168.1.5:80`
  - `192.168.1.5` → Device (IP)  
  - `:80` → Service (Web server port)  

## ✅ Summary:
  - 🌍 **IP** = Address system (where /Addressing/).
  - 📞 **TCP** = Reliable transport (how).
  - ⚡ **TCP/IP** = Core Internet protocols \ that powers the Internet.
  - 🏠 **TCP/IP Address** = [IP + Port] Usually just an IP address used with TCP.
    ## ✅ Quick Recap

-  = Addressing (Where)  
- 📞 **TCP** = Reliable Transport (How)  
- = Core Internet protocols  
- 🏠 **TCP/IP Address** = IP + Port  
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

## 📖 The OSI Model (7 Layers)

**What it is:**  
A **conceptual framework** for how systems communicate, created by ISO.  
    ✨ **Why it matters:**  
    🧩 Standardization
    🏗 Modularity 
    🔗 Interoperability 
    🪜 Layer Independence  
    🔍 Easier Debugging 
    📈 Scalability   
    🎓 Education 
    💡 Innovation  

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

## 7️⃣ Application Layer

📍 **What it is:**  
The **Application Layer** enables software applications to **use the network**.  
It provides the functionality to **send and receive data** without worrying about the lower-level details.  

- 🏆 **Top layer** in the OSI model.  
- 👨‍💻 Provides services for browsers, email clients, WhatsApp, Zoom, etc.  
- 📤 Passes requests down to the lower layers (doesn’t send raw data itself).  

### 🔹 How Data Flows
1. Browser creates an **HTTP GET request** (**Application Layer**)  
2. TCP ensures **reliable delivery** (**Transport Layer**)  
3. IP decides **where to send** (**Network Layer**)  
4. Ethernet/Wi-Fi sends **signals** (**Data Link & Physical Layers**)  

---

## 6️⃣ 🎭 Presentation Layer

📍 **What it is:**  
The **Presentation Layer** makes sure data is in a **usable format** and applies **encryption, compression, or translation** if needed.  
It acts as a **translator** between the Application (Layer 7) and Transport (Layer 4).  

### 🛠 Main Responsibilities
- 🔤 **Translation / Encoding**  
   - Converts data formats between sender and receiver.  
   - Example: EBCDIC → ASCII, UTF-8 encoding.  

- 📦 **Compression**  
   - Reduces file size for faster transfer.  
   - Example: JPEG (images), MP3 (audio), MPEG (video).  

- 🔒 **Encryption & Decryption**  
   - Protects data confidentiality.  
   - Example: **TLS/SSL** in HTTPS.  

---

### 🔹 TLS/SSL Handshake (Simplified)
```C
	Client                                    Server
	------                                    ------
	   |  SYN  ------------------------------   |
	   |       ----------------------> SYN_ACK  |
	   |  ACK  <-----------------------------   |	+-------------------------------------------------------------------------------+
	   | SYN → SYN-ACK → ACK (TCP C establish)  |	|	📦 Examples in Real Life											        |
	   |  ClientHello ----------------------->  |	|		File Formats: JPEG, PNG, MP3, MP4, PDF → standard presentation formats. |
	   |                                        |	|		Data Encoding: ASCII, UTF-8, EBCDIC.									|				
	   |  <----------------- Server Hello/i get |	|		Encryption: SSL/TLS (used in HTTPS).									|				
	   |  <------------------- Certificate      |	|		Compression: ZIP, GIF, MPEG.											|		
	   |  <----------------- Server_Hello_Done  |	+-------------------------------------------------------------------------------+
	   |                                        |
	   | Client_Key_Exchange ---------------->  |  ChangeCipherSpec ||<<
	   |  ChangeCipherSpec ------------------>  |  يتحول كلا الجانبين إلى الوضع المشفر.
	   |  Finished -------------------------->  |
	   |                                        |
	   |  <----------------- ChangeCipherSpec   |
	   |  <------------------- Finished         |
```

### 📦 Examples in Real Life
- File Formats → JPEG, PNG, MP3, MP4, PDF  
- Data Encoding → ASCII, UTF-8, EBCDIC  
- Encryption → SSL/TLS in HTTPS  
- Compression → ZIP, GIF, MPEG  

---

## 5️⃣ 🗨️ Session Layer

📍 **What it is:**  
The **Session Layer** manages and controls the **dialog (sessions)** between two devices.  
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
