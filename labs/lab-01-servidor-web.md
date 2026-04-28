# 🧪 Lab 01 - Web Server Deployment (Linux + Cloud)

## 🎯 Objective

Deploy and configure a web server using Linux, simulating a real-world cloud environment scenario.

---

## 🛠️ Technologies Used

* Linux (Ubuntu)
* Nginx
* Networking (basic)
* Monitoring (basic)
* Cloud concepts (OCI / AWS)

---

## 📋 Prerequisites

* Basic knowledge of Linux
* Access to a Linux environment (local VM or cloud instance)
* Terminal access

---

## ⚙️ Step-by-Step Implementation

### 🔹 1. Update the system

Update package lists to ensure the latest versions are installed:

```bash
sudo apt update -y
```

---

### 🔹 2. Install Nginx (Web Server)

```bash
sudo apt install nginx -y
```

---

### 🔹 3. Start and enable the service

```bash
sudo systemctl start nginx
sudo systemctl enable nginx
```

Check if it's running:

```bash
sudo systemctl status nginx
```

---

### 🔹 4. Verify access via browser

Open your browser and access:

* Local environment:

```
http://localhost
```

* Cloud environment:

```
http://YOUR_PUBLIC_IP
```

Expected result:
👉 Nginx default page ("Welcome to nginx")

---

### 🔹 5. Configure a custom web page

Edit the default HTML file:

```bash
sudo nano /var/www/html/index.html
```

Replace with:

```html
<h1>My First Web Server</h1>
<p>Deployed by Thiago Almeida</p>
```

Save:

* CTRL + X
* Y
* Enter

---

### 🔹 6. Restart the service

```bash
sudo systemctl restart nginx
```

Refresh browser to see changes.

---

### 🔹 7. Basic Monitoring

Check server status:

```bash
sudo systemctl status nginx
```

Check open ports:

```bash
sudo ss -tulnp
```

---

## ☁️ Cloud Deployment (Conceptual)

Steps to deploy in a cloud environment:

1. Create a Virtual Machine (VM)
2. Generate SSH key
3. Connect via SSH:

```bash
ssh -i key.pem ubuntu@YOUR_PUBLIC_IP
```

4. Allow inbound traffic:

* Port 22 (SSH)
* Port 80 (HTTP)

5. Repeat installation steps

---

## 📸 Evidence

(To be added)

* VM running
* SSH connection
* Browser access
* Custom page

---

## 🌍 Real World Scenario

This lab simulates a basic web server deployment used in:

* Hosting simple applications
* Internal company systems
* Initial cloud environments

---

## 📚 Key Learnings

* Linux service management
* Web server deployment
* Basic networking concepts
* Troubleshooting services
* Cloud deployment workflow

---

## 🔄 Next Steps

* Deploy in real cloud environment
* Configure multiple servers
* Implement load balancing
* Automate with Terraform

