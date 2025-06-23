

## 📌 Wireshark Filters

### What are Wireshark Filters?

Wireshark filters are used to **narrow down** the traffic being analyzed.
They help in focusing on specific packets, making the analysis faster and more efficient.

### Why are Wireshark Filters Used?

* To **quickly find** relevant data in huge traffic.
* To filter specific IPs, protocols, ports, etc.
* To analyze suspicious or targeted network traffic.
* To reduce complexity when investigating large `.pcap` files.

### 🔎 Some Common Wireshark Filters:

| Filter                      | Description                               |
| --------------------------- | ----------------------------------------- |
| `ip.addr == 192.168.1.1`    | Show packets to/from IP `192.168.1.1`     |
| `tcp.port == 80`            | Show HTTP traffic (TCP port 80)           |
| `http`                      | Show only HTTP traffic                    |
| `tcp`                       | Show only TCP traffic                     |
| `udp`                       | Show only UDP traffic                     |
| `dns`                       | Show only DNS traffic                     |
| `ssl` or `tls`              | Show only SSL/TLS traffic                 |
| `frame contains "password"` | Search for the word "password" in packets |

---

## 🛡️ What is Tor Relay?

### Tor (The Onion Router)

A privacy-focused network that anonymizes your internet traffic by routing it through multiple servers (called relays).

### Types of Tor Relays:

1. **Guard (Entry) Relay:**

   * First node in the Tor circuit.
   * Knows your IP address, but not the final destination.

2. **Middle Relay:**

   * Passes traffic along the circuit.
   * Knows only the previous and next relay, not the source or destination.

3. **Exit Relay:**

   * Last node that sends the traffic to the final destination.
   * Sees the destination but doesn’t know the sender.

---

## 🔄 Data Flow in Tor Network

```text
User → Guard Relay → Middle Relay → Exit Relay → Internet
```

### Step-by-Step:

1. **User's traffic enters the Guard Relay** (it knows your IP but not the destination).
2. The traffic is passed to the **Middle Relay** (which only knows it came from the Guard Relay and will pass to Exit).
3. The traffic exits through the **Exit Relay** to the final destination (the destination sees traffic from the Exit node, not the user).
4. Each hop decrypts one layer (like peeling an onion).

### Key Concept:

* Each relay only knows the immediate node before and after it.
* **End-to-End Encryption within the Tor Circuit** (but not necessarily to the final destination).

---
