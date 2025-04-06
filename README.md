
---

# 🐧 INTRODUCTION TO LINUX

In the dynamic landscape of technology, mastering the fundamentals is essential for anyone aspiring to excel in fields such as **DevOps, Cloud Computing, Software Development, Cybersecurity, Data Analysis/Science, AI, and QA Testing**. This project is designed to equip you with a **solid foundation in Linux**. Understanding the tech from the basics lays the groundwork for success in various tech-centric careers.

---

## 🔍 What Is Linux?

Linux is a **free, open-source operating system** similar to Windows or macOS, but it's more widely used for servers and supercomputers. It's known for its **stability, security, and flexibility**, allowing users to modify and distribute their versions.

It runs on a wide range of devices—from desktops to smartphones—and **powers much of the internet's infrastructure**. It's supported by a global community of developers who contribute to its many **distributions**, each tailored for specific needs or preferences.

---

## 📦 Linux Distributions

Linux distributions (or **distros**) are different flavors of the Linux OS built using the Linux kernel. These distros package the kernel with a range of software, libraries, and tools to provide a functional environment. Here are some examples:

### Ubuntu
Known for its **user-friendliness and ease of installation**. A great choice for newcomers.

**Use Case:** Desktop, Web Hosting, Cloud Deployments

*Alt text image placeholder*

### CentOS
Popular in **enterprise/server environments** for its **stability and long-term support**.

**Use Case:** System administration, Hosting

*Alt text image placeholder*

### Debian
Famous for its commitment to **free and open-source principles**.

**Use Case:** Versatile server and desktop use

*Alt text image placeholder*

### Fedora
A **cutting-edge distro** integrating the **latest technologies** and serving as a testing ground for RHEL.

**Use Case:** Experimentation, Development

*Alt text image placeholder*

---

## ⚙️ Installation and Initial Setup

We'll set up a **cloud-based Linux server** and access it from our **local environment** (your PC or Mac). The flow looks like this:

![Cloud Setup Diagram](2.5 access website.png)

We’ll be using **AWS EC2** (Elastic Compute Cloud) to launch a **free virtual Linux server**.

---

### 🛠 Steps to Create EC2 Instance

1. Register an AWS account  
2. Sign in and navigate to **EC2**  
3. Click **Launch Instance**  
4. Follow the wizard, select Ubuntu OS  
5. Download the `.pem` key file during the setup

![Launch Instance](2.2 ssh.png)

---

## 🔐 Connecting to the Server

### Client Tool
A **client tool** allows you to control a remote server through your terminal using commands.

### Secure Protocol
We’ll use **SSH (Secure Shell)** – a secure communication protocol.

---

### 🔧 Tools to Use

- **Windows**: MobaXterm (recommended), PuTTY, Git Bash, PowerShell  
- **Mac**: Built-in Terminal (`Applications > Utilities > Terminal`)

---

## 🚀 Connect Using SSH

Open terminal (or MobaXterm for Windows) and navigate to your `.pem` file:

```bash
cd ~/Downloads
```

List files to confirm the key is there:

```bash
ls -l
```

Now extract your server's **public IP address** from the AWS dashboard.

To connect:

```bash
ssh -i "ubuntu.pem" ubuntu@<public_ip_address>
```

Replace `<public_ip_address>` with your actual EC2 public IP.

Once connected successfully, you should see:

![SSH Connected](ssh key github account.gif)

---

## 📦 Package Managers

Linux package managers help you install, update, and remove software.

### Common Package Managers:
- `apt` → Debian, Ubuntu
- `yum` → Red Hat, CentOS (being replaced by `dnf`)
- `dnf` → Modern Red Hat, Fedora

---

### 🧱 Installing, Updating and Removing Packages

#### Update package list:
```bash
sudo apt update    # Debian/Ubuntu
sudo yum update    # Red Hat/CentOS
```

![Linux Update](ssh key pair.png)

#### Install `tree` package:
```bash
sudo apt install tree
```

Verify installation:
```bash
tree ~/Downloads
```

#### Upgrade system packages:
```bash
sudo apt upgrade
```

#### Remove a package:
```bash
sudo apt remove tree
```

---

### 💡 Practice Tip

Explore other tools to install on a Linux server. For example:

```bash
sudo apt install nginx
```

---

## 📘 Coming Up Next...

We’ll begin hands-on Linux projects involving:
- Navigating the file system
- Managing directories
- Setting file permissions
- Using Linux for real-world automation and deployments

---


