# Cloud Computing Lab 1

## Project Description

This repository contains a Cloud Computing Lab 1 project that demonstrates setting up and deploying a web application using Apache HTTP Server on a Linux system.

### Project Structure
```
cloudcomputing/
├── index.html          # Main HTML file with college and department information
├── image1.jpg          # Image file 1
├── image2.jpg          # Image file 2
├── image3.jpg          # Image file 3
├── image4.jpg          # Image file 4
└── README.md           # Project documentation
```

### Student Details
- **Name:** Laxmikant G Naik
- **USN:** 4SF24CS410
- **Department:** CSE (Computer Science and Engineering)
- **Section:** 7C

## Linux Commands Used

This lab demonstrates the following Linux commands and operations:

### 1. Create/Edit HTML File
```bash
nano index.html
```
Used to create and edit the main HTML file containing college and department information.

### 2. Update System Packages
```bash
sudo yum update -y
```
Updates all system packages to the latest version. The `-y` flag automatically answers "yes" to any prompts.

### 3. Install Apache HTTP Server
```bash
sudo yum install httpd -y
```
Installs Apache HTTP Server (httpd) which is the web server used to host the website.

### 4. Start Apache Service
```bash
sudo systemctl start httpd
```
Starts the Apache HTTP Server service to begin serving web pages.

### 5. Enable Apache Service at Boot
```bash
sudo systemctl enable httpd
```
Enables Apache to automatically start whenever the system boots up.

### 6. Move HTML File to Apache Web Directory
```bash
sudo mv ~/index.html /var/www/html/
```
Moves the HTML file from the home directory to Apache's default web directory where web content is served.

### 7. Change Ownership of Web Directory
```bash
sudo chown -R apache:apache /var/www/html/
```
Changes the ownership of the web directory to the Apache user (apache) to ensure proper permissions and security.

### 8. Restart Apache Service
```bash
sudo systemctl restart httpd
```
Restarts the Apache HTTP Server to apply any configuration changes.

## Setup Summary

The workflow follows these steps:
1. Create HTML content with student and college information
2. Update system packages
3. Install Apache HTTP Server
4. Configure Apache to start on boot
5. Deploy the HTML file to Apache's web directory
6. Set proper permissions for the web directory
7. Restart Apache to serve the content


```

## Key Concepts Covered

- **Linux File Management:** Using `nano`, `mv`, and file permissions
- **Package Management:** Using `yum` to install and update software
- **System Services:** Managing services with `systemctl`
- **Web Server Deployment:** Setting up and configuring Apache HTTP Server
- **File Permissions:** Understanding ownership and access control with `chown`

## Notes

- All commands with `sudo` require root or superuser privileges
- The Apache user (`apache`) must have read permissions on the web directory
- The web directory `/var/www/html/` is Apache's default directory for serving static content
- `systemctl` is used for managing system services in modern Linux distributions

# cloudcomputing-lab1
