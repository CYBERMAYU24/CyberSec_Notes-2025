
---

## 📌 Top 10 Nmap Commands

| Command                       | Purpose                                             |
| ----------------------------- | --------------------------------------------------- |
| `nmap <target>`               | Basic scan to find open ports                       |
| `nmap -sS <target>`           | TCP SYN scan (Stealth scan)                         |
| `nmap -sU <target>`           | UDP scan                                            |
| `nmap -sV <target>`           | Service version detection                           |
| `nmap -O <target>`            | Operating system detection                          |
| `nmap -A <target>`            | Aggressive scan (OS, services, scripts, traceroute) |
| `nmap -p <ports> <target>`    | Scan specific ports                                 |
| `nmap -Pn <target>`           | Skip host discovery (treat host as alive)           |
| `nmap -iL <list.txt>`         | Scan targets from a file                            |
| `nmap --script vuln <target>` | Run vulnerability detection scripts                 |

---

## 🛡️ What is Vulnerability?

**Vulnerability** is a weakness or flaw in a system, network, or application that can be exploited by attackers to gain unauthorized access or cause harm.

> Example: An outdated software version with known security holes.

---

## 🎯 What is a Honeypot?

A **Honeypot** is a security system designed to attract attackers by simulating a vulnerable system. It helps to:

* Detect intrusion attempts
* Study attacker behavior
* Protect real systems

---

## 📷 What is Hikvision Camera?

**Hikvision Camera** is a widely used brand of security and surveillance cameras. These are known for:

* IP-based monitoring
* Sometimes targeted in cyber-attacks due to known vulnerabilities if not updated.

---

## 📂 Useful Linux Commands

### 🔎 `file` Command

* Checks the **type of file**.
* Example:

  ```bash
  file filename.txt
  ```
* Output: ASCII text, directory, image, etc.

---

### 📦 `gunzip` Command

* Used to **extract `.gz` files**.
* Example:

  ```bash
  gunzip file.gz
  ```

---

### 📦 `tar` Command

* Used to **archive or extract tar files**.
* Example to create:

  ```bash
  tar -cvf archive.tar folder/
  ```
* Example to extract:

  ```bash
  tar -xvf archive.tar
  ```

---

### 🌳 `tree` Command

* Displays the **directory structure** in a tree-like format.
* Example:

  ```bash
  tree
  ```

---

## 🗂️ What is `/opt` Directory?

* **/opt** stands for "optional."
* It stores **third-party software** and add-on packages that are not part of the default system.

---

## 📁 `.pcap` Extension

* **.pcap** stands for **Packet Capture**.
* Used to **store captured network traffic** for analysis.
* Can be analyzed using tools like **Wireshark**.

---

