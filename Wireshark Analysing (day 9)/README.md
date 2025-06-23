
## 1. Wireshark
- **Wireshark** is a free and open-source network protocol analyzer.
- It captures and displays packets in real-time for detailed inspection.
- Used for:
  - Network troubleshooting
  - Security analysis
  - Network protocol development
  - Learning network protocols
- Supports hundreds of protocols and media types.
- Provides filtering, packet color coding, and deep inspection.

---

## 2. IDS (Intrusion Detection System)
- IDS monitors network traffic for suspicious activity and known threats.
- Types of IDS:
  - **NIDS (Network-based IDS):** Monitors network traffic.
  - **HIDS (Host-based IDS):** Monitors system activities and files.
- It can:
  - Alert administrators of potential attacks.
  - Log traffic for analysis.
- IDS tools example: Snort, Suricata.

---

## 3. SOC (Security Operations Center)
- **SOC** is a centralized unit that monitors, detects, prevents, and responds to cybersecurity incidents.
- Functions:
  - Continuous monitoring of security events.
  - Incident response and threat management.
  - Vulnerability management.
- Tools used: SIEM systems, IDS/IPS, firewalls, Wireshark, etc.

---

## 4. Opening Files from System to Wireshark
### Steps:
1. **Capture a File:** 
   - Files are usually saved with `.pcap` or `.pcapng` extensions.
2. **Open in Wireshark:**
   - Open Wireshark application.
   - Click on `File` → `Open`.
   - Browse and select the `.pcap` file.
   - Click `Open` to start analyzing the captured traffic.
3. **Analyze Packets:**
   - Use filters (like `ip.addr == 192.168.1.1`).
   - Inspect layers: Ethernet, IP, TCP/UDP, HTTP, etc.

---

## 5. db-ip.com and ip-api.com
### db-ip.com:
- A free and paid IP geolocation service.
- Provides information like:
  - IP location (Country, City)
  - ISP details
  - Latitude and Longitude
- Website: [https://db-ip.com/](https://db-ip.com/)

### ip-api.com:
- Another IP geolocation and tracking API.
- Returns data like:
  - IP address
  - City, Region, Country
  - ZIP code
  - ISP
- Supports API access for automated lookups.
- Website: [http://ip-api.com/](http://ip-api.com/)

---

