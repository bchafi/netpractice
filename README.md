<h1 align="center">🌐 NetPractice – Networking Fundamentals</h1>
<p align="center">
  <b>A beginner-friendly guide to IP, TCP, TCP/IP, and the OSI Model</b><br/>
  🚀 Understand the core protocols that power the Internet
</p>

---

## 📍 1. IP (Internet Protocol)
192.168.1.5:80

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

Example:  
- `192.168.1.5` → Device (IP)  
- `:80` → Service (Web server port)  

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
🧩 Standardization • 🏗 Modularity • 🔗 Interoperability • 🪜 Layer Independence  
🔍 Easier Debugging • 📈 Scalability • 🎓 Education • 💡 Innovation  

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

## 🖥 Application Layer Example (Google.com)

1. Browser creates an **HTTP GET request** (Application)  
2. TCP ensures **reliable delivery** (Transport)  
3. IP decides **where to send** (Network)  
4. Ethernet/Wi-Fi sends **signals** (Data Link & Physical)  

---

## ✅ Quick Recap

- 🌍 **IP** = Addressing (Where)  
- 📞 **TCP** = Reliable Transport (How)  
- ⚡ **TCP/IP** = Core Internet protocols  
- 🏠 **TCP/IP Address** = IP + Port  

---

## 📚 Resources

- [RFC 791 – IP](https://www.rfc-editor.org/rfc/rfc791)  
- [RFC 793 – TCP](https://www.rfc-editor.org/rfc/rfc793)  
- [OSI Model – Wikipedia](https://en.wikipedia.org/wiki/OSI_model)  

---

<p align="center">
  Made with ❤️ for learning and practicing <b>Networking Fundamentals</b>
</p>
