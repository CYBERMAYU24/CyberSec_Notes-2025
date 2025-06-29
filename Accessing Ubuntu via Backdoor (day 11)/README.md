
### 🗂️ `.ova` File

An `.ova` (Open Virtual Appliance) file is a pre-packaged virtual machine (VM) that includes the virtual disk, hardware settings, and other configurations. It’s used to deploy operating systems or pen-testing labs like Metasploitable, DVWA, etc., into virtualization software like VirtualBox or VMware.

---

### 🔍 `sudo arp-scan -l -I eth1`

**Purpose**: Scans the local network for active devices.

* `sudo`: Run as root for permission.
* `arp-scan`: A tool to find devices in the network using ARP packets.
* `-l`: Scan the local subnet (e.g., 192.168.1.0/24).
* `-I eth1`: Specify the interface (like `eth1`) manually.

📌 **Note on `.1` IPs**:
Most home and lab networks have `.1` as the default **gateway/router IP**. For example:

* `192.168.1.1` —> router/gateway
* Devices get `.2`, `.3`, etc.

---

### 🔎 `sudo nmap -Pn -p- <port> -vv <ipaddress>`

**Purpose**: Scan a specific port on a target without pinging first.

* `-Pn`: Skip host discovery (assume target is up).
* `-p- `: Scan all 65000 ports.
* `-vv`: Very verbose output (more details).
* `<ipaddress>`: Target IP address.

Example:

```bash
sudo nmap -Pn -p 22 -vv 192.168.1.10
```

---

### 💣 `searchsploit <service or version>`

**Purpose**: Searches for known exploits in the local **Exploit Database**.

Example:

```bash
searchsploit vsftpd 2.3.4
```

You’ll get a list of known vulnerabilities for that service/version. Can also search for shellcodes.

---

### 🧠 Exploits vs. Shellcodes

| Term          | Description                                                                                                                                                  |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Exploit**   | A script/code that takes advantage of a vulnerability to perform unintended actions (e.g., gain shell, crash system).                                        |
| **Shellcode** | A small piece of code (usually in assembly) used to open a shell on the target machine once the exploit succeeds. It’s the payload delivered by the exploit. |

---

### 🧍 Username Enumeration

**Definition**: Identifying valid usernames on a system or service.
Examples:

* Error messages revealing valid/invalid usernames.
* Timing differences in login responses.
* Enumeration via protocols like SMTP, SSH, or web forms.

---

### 🐍 Compromised Source / Backdoor / Remote Code Execution (RCE)

| Term                            | Meaning                                                                                                       |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| **Compromised Source**          | Software from a hacked source (e.g., a backdoored GitHub repo).                                               |
| **Backdoor**                    | Hidden code or method that gives attackers access later (e.g., hardcoded credentials).                        |
| **RCE (Remote Code Execution)** | A vulnerability that allows an attacker to run arbitrary code on the target machine remotely. Very dangerous. |

---

### 🌐 `sudo nmap -Pn -p- -vv -oN all-port.txt <ipaddress>`

**Purpose**: Scan all 65,535 ports on a target and save the output.

* `-Pn`: Don’t ping; assume the host is up.
* `-p-`: Scan all ports (1-65535).
* `-vv`: Very verbose.
* `-oN all-port.txt`: Save the output to a file named `all-port.txt`.

Example:

```bash
sudo nmap -Pn -p- -vv -oN all-port.txt 192.168.1.5
```

This is useful when you're trying to discover **hidden or non-standard ports** running vulnerable services.

---
Absolutely! Here's a **shortened version of the Hacking Cycle** that fits well with your previous content and keeps everything clear and compact:

---

### 🔄 Hacking Cycle (Phases of Ethical Hacking)

The **hacking cycle** is a step-by-step process attackers (and ethical hackers) follow to identify and exploit vulnerabilities in a system.

---

#### 1. 🕵️ Reconnaissance

Gathering information about the target.

* **Passive**: No direct contact (e.g., Google, WHOIS).
* **Active**: Direct probing (e.g., Nmap, ping).

---

#### 2. 🌐 Scanning & Enumeration

Identify open ports, services, and system details.

* Tools: `nmap`, `enum4linux`, `dirb`, `netcat`

---

#### 3. 💥 Gaining Access

Use exploits to enter the system (e.g., RCE, SQLi, password attacks).

* Tools: `Metasploit`, `sqlmap`, `Hydra`, `searchsploit`

---

#### 4. 🔐 Maintaining Access

Stay inside the system using backdoors, shells, or new users.

---

#### 5. 🧹 Covering Tracks

Erase logs and traces to avoid detection (used in real attacks, not in ethical reports).

---

#### 6. 📝 Reporting

(For ethical hackers) Document findings, vulnerabilities, and solutions.

---
