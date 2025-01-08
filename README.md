# Neko Rooms Installer

## Overview

This script automates the installation and configuration of **Neko Rooms**, a powerful and customizable virtual rooms platform. It sets up the required environment using **Docker**, **NGINX**, and **Certbot**, providing a secure and efficient deployment.

## Features

- Installs **Docker**, **Docker Compose**, **NGINX**, and other dependencies.
- Deploys Neko Rooms using **Docker Compose**.
- Configures **NGINX** as a reverse proxy for secure and seamless access.
- Automates **SSL certificate generation** using **Certbot**.
- Includes a **cron job** for automatic SSL renewal.
- Provides an admin management script for user authentication.

## Prerequisites

Ensure the following before running the script:

- **Operating System**: Debian 9+/Ubuntu 18.04+.
- **Hardware Requirements**:
  - At least 2GB memory, 4 CPU cores, and 8GB disk space.
- **Network Requirements**:
  - Free TCP ports 80 and 443.
  - Free UDP port range 59000–59099.
  - A domain name pointing to the server’s public IP.

## Installation

1. Download the script using **curl** or **wget**:
   ```bash
   # Using curl
   curl -O https://raw.githubusercontent.com/H1ghSyst3m/Neko-Room-Installer/main/neko-room-installer.sh
   
   # Using wget
   wget https://raw.githubusercontent.com/H1ghSyst3m/Neko-Room-Installer/main/neko-room-installer.sh
   ```

2. Run the installer script:
   ```bash
   sudo bash neko-room-installer.sh
   ```

3. Follow the prompts to configure your domain, email, and other settings.

## Access

Once the installation is complete:

- Public Rooms: `https://<your-domain>/<path-prefix>/<room-id>`
- Admin Panel: Restricted and password-protected.

## Admin Management

Use the included script to manage admin users:
- Add a user:
  ```bash
  sudo /usr/local/bin/manage_htpasswd.sh add <username>
  ```
- Remove a user:
  ```bash
  sudo /usr/local/bin/manage_htpasswd.sh remove <username>
  ```
- Change a user password:
  ```bash
  sudo /usr/local/bin/manage_htpasswd.sh change_password <username>
  ```
- List users:
  ```bash
  sudo /usr/local/bin/manage_htpasswd.sh list
  ```

---

For detailed usage and troubleshooting, refer to the script comments or consult the Neko Rooms documentation.
