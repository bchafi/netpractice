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

#### 📍 Advantages over IPv4:
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

➡️ **Data Flow:**
Data → TCP (split/check) → IP (address/route) → Internet → TCP (rebuild) → App
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

## 🖥 Application Layer in OSI Model:
    - The Application layer enables applications to use the network.
    - is the top layer in this model and takes care of network communication.
    - The application layer provides the functionality to send and receive data from users.
    - It gives applications (like browsers, email clients, Zoom, WhatsApp) a way to request network services without worrying about the lower details.
  Passes Data to Lower Layers
    \- The Application layer doesn’t send raw data directly over the internet.
    \- Instead, it hands its data (like an HTTP request) to the Transport Layer (TCP/UDP).
    \- Example flow when you open www.google.com in your browser:
    \- Browser creates an HTTP GET request (Application Layer).
    \- Passes it to TCP (Transport Layer) → ensures reliable delivery.
    \- TCP hands it to IP (Network Layer) → decides where to send.
    \- IP hands it to Ethernet/Wi-Fi (Data Link & Physical Layers) → sends the bits.
  Example: 
    1. Browser creates an **HTTP GET request** (Application)  
    2. TCP ensures **reliable delivery** (Transport)  
    3. IP decides **where to send** (Network)  
    4. Ethernet/Wi-Fi sends **signals** (Data Link & Physical)  

---

🎭 Presentation Layer (OSI Layer 6)
	The Presentation Layer is responsible for how data is presented, formatted, and sometimes encrypted, so that applications can understand it.
	  It acts like a translator between the Application Layer (Layer 7) and the Transport Layer (Layer 4).
  🛠 Main Responsibilities
	-> Translation / Encoding
		* Converts data into a format that the receiving application can understand.
			Example: Convert EBCDIC (used by old IBM systems) into ASCII.(Extended Binary Coded Decimal Interchange Code).
	-> Compression
		* Reduces data size to save bandwidth and improve speed.
			Example: JPEG, MP3, MPEG compression.
	-> Encryption & Decryption
		* Protects data for confidentiality.
			Example: TLS/SSL encryption in HTTPS.
		=> TLS/SSL Handshake
		Client                                     Server
		------                                     ------
			|  SYN  ------------------------------   |
			|       ----------------------> SYN_ACK  |
			|  ACK  <-----------------------------   |      +-------------------------------------------------------------------------------+
			| SYN → SYN-ACK → ACK (TCP C establish)  |		|	📦 Examples in Real Life											        |
			|  ClientHello ----------------------->  |		|		File Formats: JPEG, PNG, MP3, MP4, PDF → standard presentation formats. |
			|                                        |		|		Data Encoding: ASCII, UTF-8, EBCDIC.									|				
			|  <----------------- Server Hello/i get |		|		Encryption: SSL/TLS (used in HTTPS).									|				
			|  <------------------- Certificate      |		|		Compression: ZIP, GIF, MPEG.											|		
			|  <----------------- Server_Hello_Done  |      +-------------------------------------------------------------------------------+
			|                                        |
			| Client_Key_Exchange ---------------->  |  ChangeCipherSpec ||<<
			|  ChangeCipherSpec ------------------>  |  يتحول كلا الجانبين إلى الوضع المشفر.
			|  Finished -------------------------->  |
			|                                        |
			|  <----------------- ChangeCipherSpec   |
			|  <------------------- Finished         |

---

🗨️ Session Layer (OSI Layer 5): "Analogy: Like a moderator keeping a conversation orderly"
	- Without it → chaos: overlapping talk, no recovery from crashes, broken logins.
	The Session Layer manages and controls the dialog (sessions) between two devices.
	  It decides who talks, when they talk, and for how long.				+---------------------------------------------------+			
	Example:																| 📦 Real-Life Examples		                  		|
		Think of it as the “conversation manager” of a network connection   |    -> NetBIOS (Network Basic Input/Output System) |
	🛠 Main Responsibilities   		 										|    -> RPC (Remote Procedure Call)	             	|
	  -> Establishing Sessions:												|    -> SQL Sessions when connected to a database   |	
		 * Starts the communication between two devices.					|    -> API sessions with authentication tokens	    |		
		    Example: Logging into a remote server with SSH.					|    -> SSH or RDP sessions for remote access       |				
	  -> Maintaining Sessions:												+---------------------------------------------------+
		 * Keeps track of ongoing communication.										
		    Example: A video call staying active while you talk.									
	  -> Synchronizing:																			
		 * Adds checkpoints in long transmissions, so if a crash happens, you don’t restart from scratch.
		    Example: Downloading a 2 GB file → if interrupted, resume from 1.5 GB instead of starting over.
	  -> Terminating Sessions:
		 * Gracefully ends communication when one side finishes.
		    Example: Clicking “Log Out” ends the session.

---

## 📚 Resources

- [RFC 791 – IP](https://www.rfc-editor.org/rfc/rfc791)  
- [RFC 793 – TCP](https://www.rfc-editor.org/rfc/rfc793)  
- [OSI Model – Wikipedia](https://en.wikipedia.org/wiki/OSI_model)  

---

<p align="center">
  Made with ❤️ for learning and practicing <b>Networking Fundamentals</b>
</p>
