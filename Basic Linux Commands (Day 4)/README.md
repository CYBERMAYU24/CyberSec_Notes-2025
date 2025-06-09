

# Basic Linux Commands

### 1. `ls`
- Lists files and directories in the current working directory.
- Example:
  ```bash
  ls

### 2. `whoami`

* Displays the current logged-in username.
* Example:

  ```bash
  whoami
  ```

### 3. `hostname`

* Shows the system's hostname.
* Example:

  ```bash
  hostname
  ```

### 4. `sudo su`

* Switches to the superuser (root) account.
* Example:

  ```bash
  sudo su
  ```
  
# How to Add a New User in Linux Using `useradd`

## 📌 Step 1: Open Terminal
- Make sure you have **sudo (admin) access**.

---

## 📌 Step 2: Create a New User with Home Directory
Use the `useradd` command with the `-m` option to create a user and their home directory:
```bash
sudo useradd -m newusername

**Example:**

```bash
sudo useradd -m john
```

> 🔹 `-m` ensures the home directory `/home/john` is created.

---

## 📌 Step 3: Set Password for the New User

```bash
sudo passwd john
```

* Enter the new password and confirm it.

---

## 📌 Step 4: Add User to a Specific Group (Optional)

If you want to add the user to a specific group:

```bash
sudo usermod -aG groupname username
```

**Example:**

```bash
sudo usermod -aG sudo john
```

> 🔹 This gives **sudo (admin) privileges** to the user.

---

## 📌 Step 5: Switch to the New User

Use this command to log in as the new user:

```bash
su - username
```

**Example:**

```bash
su - john
```

> 🔹 The `-` loads the user's environment (like their home folder, PATH, etc.).

---

## 🎯 Quick Reference Table

| Command                               | Purpose                             |
| ------------------------------------- | ----------------------------------- |
| `sudo useradd -m username`            | Create new user with home directory |
| `sudo passwd username`                | Set user password                   |
| `sudo usermod -aG groupname username` | Add user to a group                 |
| `su - username`                       | Switch to the new user              |

---

### 7. `df -h`

* Shows disk space usage in human-readable format.
* Example:

  ```bash
  df -h
  ```

### 8. `du -sh`

* Shows the total size of a directory.
* Example:

  ```bash
  du -sh /home/username
  ```

### 9. `htop`

* Interactive process viewer (like Task Manager in Windows).
* To run:

  ```bash
  htop
  ```

---

## Network Commands

### 10. `ping` Command

* Used to test network connectivity.
* Example:

  ```bash
  ping 8.8.8.8 -c 3
  ```
* `8.8.8.8` is Google’s public DNS server.
* `-c 3` limits the ping to 3 packets.

---

## DNS and DNS Server Function

* **DNS (Domain Name System)** translates domain names (like google.com) into IP addresses.
* **DNS Server** is responsible for resolving domain names to IP addresses.

---

## Other Networking Concepts

### 11. `ifconfig`

* Displays network interfaces and IP addresses.
* Example:

  ```bash
  ifconfig
  ```

### 12. Subnet

* Subnetting divides a network into smaller parts.
* Helps in managing IP addresses and improves security and performance.

### 13. IPv4 vs IPv6

| Feature        | IPv4                    | IPv6                                    |
| -------------- | ----------------------- | --------------------------------------- |
| Address Length | 32-bit                  | 128-bit                                 |
| Example        | 192.168.1.1             | 2001:0db8:85a3:0000:0000:8a2e:0370:7334 |
| Address Space  | \~4.3 billion addresses | Almost infinite                         |

### 14. Localhost

* Refers to the local machine.
* IP Address: `127.0.0.1`

---

## Hacking Cycle in Cybersecurity (5 Stages)

1. **Reconnaissance**
   Gathering information about the target.

2. **Scanning**
   Finding open ports, vulnerabilities, and entry points.

3. **Gaining Access**
   Exploiting vulnerabilities to get into the system.

4. **Maintaining Access**
   Installing backdoors or creating new user accounts to keep control.

5. **Clearing Tracks**
   Deleting logs and traces to avoid detection.

---

## Reverse Engineering

* Process of analyzing software or hardware to understand its design, code, and functionality.
* Often used to find vulnerabilities or analyze malware.

---

## Post-Exploitation

* Actions taken after gaining access to a system.
* Goals:

  * Extracting data
  * Maintaining access
  * Pivoting to other systems
  * Establishing long-term control

---

```
