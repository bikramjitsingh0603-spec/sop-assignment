# Standard Operating Procedure (SOP)

## Setup a Virtual Linux Server for Web Application Testing

**Company Name:** MITT IT Support Lab
**Department:** System Administration
**Prepared By:** Bikramjit Singh
**Version:** 1.0
**Date:** March 2026

---

# Approval Table

| Version | Date       | Prepared By     | Approved By |
| ------- | ---------- | --------------- | ----------- |
| 1.0     | March 2026 | Bikramjit Singh | IT Manager  |

---

# Purpose

The purpose of this document is to describe the standard procedure for setting up a virtual Linux server that can be used to test web applications in a controlled and secure environment. This ensures consistency and reliability during development and testing activities.

---

# Scope

This procedure applies to system administrators, IT students, and support staff responsible for preparing Linux virtual machines for web application testing purposes.

---

# Objectives

* Create a virtual Linux server environment
* Configure hostname and networking
* Install required software packages
* Prepare server for web application deployment
* Verify functionality of testing environment

---

# System Requirements

### Hardware Requirements

* Minimum 2 CPU cores
* 4 GB RAM
* 40 GB storage space
* Internet connectivity

### Software Requirements

* VirtualBox or VMware Workstation
* Ubuntu Server 22.04 LTS
* Apache Web Server
* MySQL Database Server
* PHP

---

# Linux Server Configuration Details

| Setting      | Value                  |
| ------------ | ---------------------- |
| Hostname     | linux-web-lab1        |
| IP Address   | 192.168.1.25           |
| OS Version   | Ubuntu Server 22.04    |
| Network Type | NAT or Bridged Adapter |

---

# Accountability Matrix

| Task                  | Responsible Person   | Approval Authority |
| --------------------- | -------------------- | ------------------ |
| VM Creation           | System Administrator | IT Manager         |
| OS Installation       | System Administrator | IT Manager         |
| Software Installation | Support Team         | Supervisor         |
| Testing               | QA Team              | Project Lead       |

---

# Definitions

**Virtual Machine:** A software-based computer running inside another operating system.

**Web Server:** Software that delivers web pages to users.

**Apache:** Open-source web server software.

**MySQL:** Database server used for storing application data.

---

# Procedure Steps

## Step 1: Install Virtualization Software

Download and install VirtualBox or VMware Workstation on the host computer.

---

## Step 2: Create Virtual Machine

Open virtualization software and create a new virtual machine with:

* 2 CPU cores
* 4 GB RAM
* 40 GB disk space

Select Ubuntu Server ISO file as installation media.

---

## Step 3: Install Ubuntu Server

Start the virtual machine and follow installation instructions:

* Select language
* Configure keyboard layout
* Set hostname as **linux-web-lab1**
* Create administrator username and password

Complete installation and reboot system.

---

## Step 4: Configure Network Settings

Assign static IP address using netplan configuration file:

Example:

```
sudo nano /etc/netplan/00-installer-config.yaml
```

Apply configuration:

```
sudo netplan apply
```

Verify connection:

```
ip a
```

---

## Step 5: Update System Packages

Run system update command:

```
sudo apt update && sudo apt upgrade -y
```

---

## Step 6: Install Apache Web Server

Install Apache:

```
sudo apt install apache2 -y
```

Verify installation:

```
systemctl status apache2
```

Test in browser using server IP address.

---

## Step 7: Install MySQL Server

Install MySQL:

```
sudo apt install mysql-server -y
```

Secure database installation:

```
sudo mysql_secure_installation
```

---

## Step 8: Install PHP

Install PHP and required modules:

```
sudo apt install php libapache2-mod-php php-mysql -y
```

Restart Apache service:

```
sudo systemctl restart apache2
```

---

## Step 9: Test Web Server Functionality

Create test file:

```
sudo nano /var/www/html/info.php
```

Add:

```
<?php phpinfo(); ?>
```

Open browser:

```
http://192.168.1.25/info.php
```

Confirm PHP test page loads successfully.

---

# Verification Checklist

* Virtual machine created successfully
* Linux installed correctly
* Network configured properly
* Apache installed and running
* MySQL installed
* PHP working correctly

---

# References

Ubuntu Official Documentation
Apache Documentation
MySQL Documentation

---

# Revision History

| Version | Date       | Changes                 |
| ------- | ---------- | ----------------------- |
| 1.0     | March 2026 | Initial version created |
