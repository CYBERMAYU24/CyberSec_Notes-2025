# 🧪 Day 3: Downloading Kali Linux for Windows 64-bit

## 🖥️ VirtualBox for Windows 64-bit

📥 **Direct Download Link for VirtualBox (Windows 64-bit):**  
[Download VirtualBox](https://download.virtualbox.org/virtualbox/7.0.18/VirtualBox-7.0.18-162988-Win.exe)

✅ This is the latest stable version as of June 2025.

---

## 🐉 Kali Linux ISO for Windows 64-bit (Installer Version)

📥 **Direct Download Link for Kali Linux ISO (64-bit):**  
[Download Kali Linux ISO](https://cdimage.kali.org/kali-2024.1/kali-linux-2024.1-installer-amd64.iso)

✅ This is the standard 64-bit **installer ISO** (not live boot), ideal for installing into VirtualBox.

---

## ⚙️ Suggested VM Configuration

| Setting         | Value                |
|------------------|----------------------|
| OS Type          | Linux                |
| Version          | Debian (64-bit)      |
| Memory (RAM)     | 4096 MB              |
| CPUs             | 2                    |
| Video Memory     | 128 MB               |
| Storage Size     | 30 GB (dynamic)      |
| Network Adapter  | NAT or Bridged       |

---

> ⚠️ Always verify hashes if you’re downloading from a new source. These are **official direct links** from [virtualbox.org](https://www.virtualbox.org/) and [kali.org](https://www.kali.org/).


---

## 🧠 GitHub Definition

**GitHub** is a cloud-based platform for hosting, sharing, and collaborating on code using **Git**. Developers use it to manage code, issues, and workflows efficiently.

🔗 [https://github.com](https://github.com)

---

## 💙 Lovable.dev

**[Lovable.dev](https://lovable.dev)** is a minimalist developer portfolio builder that lets you create a beautiful, fast-loading, one-page site with:

- GitHub integration
- Custom links & descriptions
- Dark mode
- Drag & drop interface

Perfect for showcasing projects, resumes, and social profiles in a clean format.

---

## 📄 What is a `README.md` File?

A **README.md** is the front page of a GitHub repo. It includes:

- What the project is
- How to install and run it
- Features and credits
- Examples and contact info

Written in **Markdown**, a lightweight text formatting language.

---

## 🖥️ MCP Server in AI

**MCP (Multi-Client Processing)** in AI refers to server-side architectures that handle multiple user/model inference requests concurrently. Useful in:

- Model serving at scale
- Distributed AI systems
- High-performance AI APIs

---

## 🧠 RAG in AI (Retrieval-Augmented Generation)

**RAG** combines retrieval and generation:

1. Fetch documents (via search)
2. Use a language model (like GPT) to generate answers using those docs

Used in:
- Chatbots
- Smart assistants
- Research tools

---

## 🍴 Forking a Repo

Forking a repo means creating your own copy of someone else’s project on GitHub. You can:

- Modify it freely
- Push changes
- Submit a pull request

Great for open-source contribution.

---

## 🧠 Kernel

The **kernel** is the core program of the operating system. It manages:

- Hardware communication
- Processes and memory
- File systems and security

---

## 💻 KVM (Kernel-based Virtual Machine)

**KVM** allows Linux systems to act as hypervisors for running virtual machines. It's built into the Linux kernel and works with tools like **QEMU**.

- Used in enterprise virtual infrastructure
- Highly efficient for Linux and Windows VMs

---

## 💥 Buffer Overflow

**Buffer overflow** is when more data is written into a buffer than it can hold, causing it to overwrite adjacent memory. Attackers exploit this to:

- Execute arbitrary code
- Crash apps
- Gain unauthorized access

---

## 🔐 What is `sudo`?

**`sudo`** = **Superuser Do**

Used to run administrative commands as root.

Example:
```bash
sudo apt install nmap

```
---

## 🛡️ Privileges in Kali Linux

In Kali Linux (and other Linux systems), **privileges** determine what actions a user can perform.

- **Root user**: Has full administrative access. Can read, write, modify, and delete any file or configuration.
- **Standard user**: Has limited access. Can only manage files and processes they own.
- Use `sudo` to execute commands with temporary root privileges.

> ⚠️ Always use `sudo` carefully — incorrect commands as root can break your system.

---

## 📦 APT in Kali Linux

**APT (Advanced Package Tool)** is the command-line tool used to install, update, upgrade, and remove software in Kali Linux (Debian-based distros).

### Common APT commands:
```bash
sudo apt update         # Fetches the list of available updates
sudo apt upgrade        # Installs available updates
sudo apt install nmap   # Installs nmap package
sudo apt remove nmap    # Removes nmap
sudo apt search apache  # Searches for apache-related packages
````

---

## 📁 `pwd` Command

`pwd` stands for **Print Working Directory**.

It shows your current directory in the terminal session.

### Example:

```bash
$ pwd
/home/kali/Desktop
```

Useful for knowing where you are in the file system, especially when navigating or scripting.

---

