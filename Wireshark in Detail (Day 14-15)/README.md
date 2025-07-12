
---

# 📡 Network Protocols Explained

---

## **1. UDP (User Datagram Protocol)**

### 🔸 What is UDP?

UDP is a **connectionless**, **lightweight transport protocol** in the TCP/IP suite. It sends messages, called **datagrams**, without establishing a connection.

### 🔸 Why Use UDP if It’s Unreliable?

Despite lacking reliability (no guarantee of delivery, ordering, or duplicate protection), UDP is still widely used because of:

* **Low latency** (faster than TCP)
* **No connection overhead**
* **Broadcast and multicast support**
* **Suitability for real-time applications**

### 🔸 Where is UDP used?

* **Live video/audio streaming** (e.g., Zoom, Skype)
* **Online gaming**
* **DNS (Domain Name System)**
* **VoIP (Voice over IP)**
* **TFTP (Trivial File Transfer Protocol)**

---

## **2. TCP (Transmission Control Protocol)**

### 🔸 What is TCP?

TCP is a **connection-oriented**, **reliable** transport protocol. It ensures:

* **Guaranteed delivery**
* **Packet ordering**
* **Error checking**
* **Congestion control**

### 🔸 Where is TCP used and Why?

Used when **data integrity** and **order** are more important than speed.

#### ✅ TCP Use Cases:

* **Web browsing (HTTP/HTTPS)**
* **Email (SMTP, IMAP, POP3)**
* **File transfers (FTP, SFTP)**
* **Remote connections (SSH, Telnet)**

TCP is essential when:

* Data must arrive **intact and in order**
* **Retransmission** is acceptable in case of errors

---

## **3. TLSv1.2 (Transport Layer Security version 1.2)**

### 🔸 What is TLSv1.2?

TLS 1.2 is a **security protocol** that provides:

* **Encryption**
* **Authentication**
* **Data integrity**
  It operates **on top of TCP** and is used to secure communication over networks.

### 🔸 Where is TLS 1.2 used?

* **HTTPS websites** (SSL certificates)
* **Email encryption**
* **Secure APIs**
* **VPNs**
* **Online banking and transactions**

### 🔐 Why TLS is important?

* Prevents **man-in-the-middle attacks**
* Ensures **data confidentiality**

> TLS 1.2 is still widely supported though TLS 1.3 is now the latest and more secure version.

---

## **4. WireGuard**

### 🔸 What is WireGuard?

WireGuard is a **modern, lightweight, and fast VPN protocol** designed for ease of use and performance.

### 🔸 Why does it show up even without a VPN connection?

* Some **operating systems (like Android 12+)** include WireGuard modules by default.
* **Apps with VPN permission** might load WireGuard drivers, even if not connected.
* You may have installed an app (like AdGuard, NetGuard, or Mullvad) that uses or checks for WireGuard even in background.

> It doesn’t mean you are connected to a VPN — just that WireGuard support is available or initialized.

---

# **5. ARP Protocol (Address Resolution Protocol)**

## 📌 What is ARP?

**ARP (Address Resolution Protocol)** is a **network layer protocol** used to **map an IP address to a MAC address** on a local area network (LAN).

It allows devices in the same network to discover each other by linking **Layer 3 (IP address)** with **Layer 2 (MAC address)**.

---

## 🔄 Why Do We Need ARP?

Devices use **IP addresses** to identify each other over a network, but to actually **send data on an Ethernet or Wi-Fi LAN**, they must use **MAC addresses**.

So, when a device wants to send a packet to another device on the same network and knows only the IP address, it uses ARP to find out the destination’s MAC address.

---

## ⚙️ How ARP Works (Step-by-Step)

Let’s say **Host A** wants to communicate with **Host B**, which is in the same local network.

1. **Host A checks its ARP cache** (local table of IP-MAC mappings).
2. If Host B's MAC is **not found**, Host A broadcasts an ARP request:

   * "Who has IP `192.168.1.10`? Tell `192.168.1.5`"
3. **All devices on the network receive** the request.
4. **Host B** sees its IP in the request and responds:

   * "I have IP `192.168.1.10`, my MAC is `00:1A:2B:3C:4D:5E`"
5. **Host A stores** this mapping in its ARP cache.
6. Host A now sends the actual data to Host B using the resolved MAC address.

---

## 📋 ARP Table (ARP Cache)

Each device maintains an **ARP table**, a temporary list of IP addresses and their corresponding MAC addresses.

```plaintext
IP Address        MAC Address
192.168.1.1       00:11:22:33:44:55
192.168.1.10      00:1A:2B:3C:4D:5E
```

* Entries are stored temporarily and may expire after a few minutes.
* ARP entries can be **static** (manually set) or **dynamic** (learned via ARP requests).

---

## 🧪 Types of ARP

| ARP Type               | Description                                                                                    |
| ---------------------- | ---------------------------------------------------------------------------------------------- |
| **Request**            | Broadcast message asking "Who has this IP?"                                                    |
| **Reply**              | Unicast response providing the MAC address                                                     |
| **Gratuitous ARP**     | Sent by a device to announce its IP-MAC binding (e.g., during startup or IP change)            |
| **Proxy ARP**          | A router answers ARP requests on behalf of another device (common in networks with subnetting) |
| **Reverse ARP (RARP)** | Old protocol used to find the IP when only MAC is known (mostly obsolete)                      |

---

## ⚠️ ARP Spoofing (ARP Poisoning)

### What is it?

An attacker **sends fake ARP messages** to trick devices into updating their ARP tables with the wrong MAC address.

### 🔍 Example:

* Attacker pretends to be the **router/gateway**:

  * Maps router IP `192.168.1.1` to attacker’s MAC `AA:BB:CC:DD:EE:FF`
* Now, all traffic meant for the router is sent to the attacker.

### 🔴 Consequences:

* **Man-in-the-Middle (MITM)** attacks
* **Data theft** (passwords, private messages)
* **Session hijacking**
* **Denial of service**

---

## 🛡️ How to Prevent ARP Spoofing

| Method                       | Description                                         |
| ---------------------------- | --------------------------------------------------- |
| **Static ARP entries**       | Manually set IP-MAC mappings (not scalable)         |
| **ARP monitoring tools**     | Detect changes in ARP tables (e.g., Arpwatch, XArp) |
| **Switch security features** | Like Dynamic ARP Inspection (DAI) on Cisco switches |
| **Use encrypted protocols**  | TLS/HTTPS to protect data even if intercepted       |
| **Segmentation/VLANs**       | Isolate critical systems to reduce attack surface   |


---

## ✅ Final Note

ARP is essential for **basic networking** within a LAN, but it’s also inherently insecure due to lack of authentication. While it enables seamless communication, it's important to **monitor and secure** ARP traffic to avoid exploitation.

---

