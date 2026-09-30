# AWS EC2 Task 3 — Install and Configure Apache Web Server

## Overview

This task involved installing and configuring the Apache web server on an Ubuntu EC2 instance running on AWS.

## Objectives

- Launch an AWS EC2 Ubuntu instance.
- Connect to the instance using SSH.
- Install Apache2.
- Verify that Apache is running.
- Test Apache locally from the EC2 server.
- Access the Apache web server through the instance's public IP address.
- Verify that Apache starts automatically.

## Steps Taken

### 1. Launched an EC2 Instance

Created a new Ubuntu EC2 instance for Task 3.

The Security Group was configured with:

- SSH — TCP port 22 — My IP
- HTTP — TCP port 80 — Anywhere
- HTTPS — TCP port 443 — Anywhere

### 2. Connected to the EC2 Instance

Connected to the Ubuntu EC2 instance using SSH and the existing EC2 key pair.

### 3. Updated the Server

Updated the Ubuntu package lists using:

```bash
sudo apt update

### 4. Installed Apache

Installed Apache2 using:

sudo apt install apache2 -y

### 5. Verified Apache Service

Checked the Apache service status using:

sudo systemctl status apache2

The service was confirmed to be:

Active: active (running)

### 6. Tested Apache Locally

Tested the Apache web server from inside the EC2 instance:

curl http://localhost

The command returned the Apache HTML page successfully.

### 7. Tested Apache Through the Public IP

Opened the EC2 instance's public IPv4 address in a web browser:

http://YOUR-PUBLIC-IP

The Apache2 Ubuntu Default Page was displayed successfully.

### 8. Verified Apache Starts Automatically

Checked whether Apache was enabled to start automatically:

sudo systemctl is-enabled apache2

The result was:

enabled

#Difficulty Faced

No major technical difficulty was encountered during the Apache installation.

The main configuration required was allowing HTTP traffic on port 80 through the EC2 Security Group so that the Apache web server could be accessed from a browser.

#What I Learned
How to install Apache2 on Ubuntu.
How to manage services using systemctl.
How to check whether a service is running.
How to test a web server using curl.
How AWS Security Groups control access to web server ports.
How to access an Apache web server through an EC2 public IP address.
How to verify that Apache is enabled to start automatically.

#Verification

Apache was successfully installed, started, and accessed through the EC2 public IP address.

The Apache2 Ubuntu Default Page was successfully displayed in the browser.

Conclusion

Task 3 was successfully completed. Apache was installed and configured on an AWS EC2 Ubuntu instance, verified locally, and successfully accessed through the public IP address.
