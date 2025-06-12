

---

## 🔍 Nmapping (Nmap)

* **Nmap (Network Mapper)** is a free and powerful tool used to scan and discover hosts, open ports, and services in a network.
* It helps hackers and security professionals understand what machines are active and how they are configured.
* Example:

  ```bash
  nmap 192.168.1.1
  ```
* ✅ Used for: Port scanning, OS detection, network mapping.

---

## 🐳 Docker

* **Docker** is a tool used to create, deploy, and run applications using containers.
* Containers are lightweight, portable environments that run software consistently across different systems.
* Example:

  ```bash
  docker run -it ubuntu
  ```
* ✅ Benefits: Faster deployment, isolated environments, easy scalability.

---

## 🖥️ Uname -a Command

* Displays detailed information about the system.
* Example:

  ```bash
  uname -a
  ```
* ✅ Output includes: Kernel name, version, machine type, processor type, etc.
* 📌 Useful for system identification and troubleshooting.

---

## 🏃‍♂️ Run -it Command

* The `-it` option in Docker runs a container in **interactive mode** with a terminal.
* Example:

  ```bash
  docker run -it ubuntu bash
  ```
---
  ## -d Command

* ✅ The container runs in the background."Detached Mode"
You won’t see any live terminal output.
* Example:

  ```bash
  docker run -d ubuntu
  ```
---

## ☸️ Kubernetes

* **Kubernetes** is an open-source system to automate the deployment, scaling, and management of containerized applications.
* It manages clusters of Docker containers.
* ✅ Key features: Load balancing, self-healing, automatic scaling.

---

## 🔁 CI/CD Pipeline

* **CI/CD** stands for **Continuous Integration / Continuous Deployment.**
* It is a method to frequently deliver apps to customers by introducing automation.
* ✅ CI: Automatically integrates code changes.
* ✅ CD: Automatically deploys code to production.
* Example Tools: Jenkins, GitLab CI, CircleCI.

---

## 🌐 SaaS (Software as a Service)

* Software is provided over the Internet as a **service**.
* You don’t need to install or maintain it.
* Example: Google Docs, Gmail, Zoom.
* ✅ Benefits: Accessible from anywhere, automatic updates.

---

## 🌍 MaxMind.com

* A website that offers **IP geolocation services.**
* Helps track the approximate physical location of an IP address.
* ✅ Used in: Fraud detection, content localization, security analytics.
* Website: [https://www.maxmind.com](https://www.maxmind.com)

---

## 🛡️ WafW00f

* A tool that identifies and detects **Web Application Firewalls (WAFs).**
* Useful for penetration testers to know what type of security is in front of a web server.
* Example:

  ```bash
  wafw00f https://example.com
  ```
* ✅ Helps in bypassing or testing WAF rules effectively.

---

---


## 📊 Uptime Kuma

**Uptime Kuma** is a free, self-hosted monitoring tool that checks the uptime and availability of your websites, servers, and services.

* **Purpose:** It notifies you if your services are down.
* **Features:**

  * Beautiful Web UI
  * Customizable alerts (via Telegram, Discord, email, etc.)
  * HTTP(s), TCP, Ping, and Docker container monitoring.
* **Example Use:** Monitor your website `example.com` and get a Telegram alert if it goes offline.

![Uptime Kuma Example](https://raw.githubusercontent.com/louislam/uptime-kuma/master/public/icon.svg)

---

## 🌐 Open Web UI Docker

When running a **Dockerized** app (like Uptime Kuma), many tools provide a **Web UI (User Interface)** to easily manage and visualize the service.

* **How it works:**

  * The Docker container exposes a specific **port** (like `http://localhost:3001`).
  * You can open this link in your browser to access the application dashboard.
* **Example Command:**

  ```bash
  docker run -d -p 3001:3001 --name uptime-kuma louislam/uptime-kuma
  ```

  You can then open the web UI at: `http://localhost:3001`

---

## 🚪 Docker Nginx Reverse Proxy

**Nginx Reverse Proxy** forwards client requests to backend services running in Docker.

* **Why Use It?**

  * To route multiple services on the same server using different domains or subdomains.
  * For example:

    ```
    yourdomain.com --> Uptime Kuma container
    api.yourdomain.com --> API container
    ```

* **Benefits:**

  * Centralized request management
  * SSL termination (HTTPS)

* **Example Docker Setup:**

  ```yaml
  services:
    nginx:
      image: nginx
      ports:
        - "80:80"
        - "443:443"
      volumes:
        - ./nginx.conf:/etc/nginx/nginx.conf
  ```

  You can configure Nginx to direct traffic to your running Docker containers based on the request domain or path.

---

## 🔍 `sudo nmap -O <ip/domain>`

**Nmap** (Network Mapper) is a powerful tool for network scanning and security auditing.

* **Command:**

  ```bash
  sudo nmap -O <ip/domain>
  ```

* **Purpose:**
  Detects the **operating system (OS)** of the target machine.

* **Flags:**

  * `sudo` → Needed because OS detection often requires elevated permissions.
  * `-O` → Enables **OS detection**.

* **Example:**

  ```bash
  sudo nmap -O example.com
  ```

* **Output:**

  * Open ports
  * Detected operating system
  * Network details

---

### 🚀 Summary Table

| Term/Command               | Purpose                            | Example                               |
| -------------------------- | ---------------------------------- | ------------------------------------- |
| Uptime Kuma                | Monitor uptime                     | Web dashboard on `localhost:3001`     |
| Open Web UI Docker         | Access web interface of Docker app | Run container and open in browser     |
| Docker Nginx Reverse Proxy | Route multiple apps via domains    | Forward `yourdomain.com` to container |
| sudo nmap -O               | Scan OS of IP/domain               | `sudo nmap -O example.com`            |

---

