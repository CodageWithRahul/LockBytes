# 🔐 LockBytes

### Secure. Private. USB-Based.

**LockBytes** is a Windows desktop application designed to protect your personal and sensitive files using strong encryption and a **USB-based vault system**.

LockBytes is built with an **offline-first philosophy** — your files can be encrypted, decrypted, and managed locally without requiring an internet connection.

> **Your files. Your vault. Your control.**

---

<p align="center">

**🔒 AES-256-GCM**   •   **🛡️ Argon2id**   •   **💾 USB Vault**   •   **☁️ Optional Recovery**

</p>

<p align="center">
  <a href="https://github.com/CodageWithRahul/LockBytes/releases/latest">
    <img src="https://img.shields.io/github/v/release/CodageWithRahul/LockBytes?style=for-the-badge&label=Latest%20Release" alt="Latest Release">
  </a>
  <a href="https://github.com/CodageWithRahul/LockBytes/releases">
    <img src="https://img.shields.io/github/downloads/CodageWithRahul/LockBytes/total?style=for-the-badge&label=Downloads" alt="Downloads">
  </a>
  <img src="https://img.shields.io/badge/Platform-Windows-0078D4?style=for-the-badge" alt="Windows">
  <img src="https://img.shields.io/badge/Version-1.0.0-success?style=for-the-badge" alt="Version 1.0.0">
</p>

---

## 📌 Overview

LockBytes provides a simple way to secure sensitive files without making cloud storage a requirement.

Unlike applications that depend entirely on online services, LockBytes keeps its **core encryption and vault workflows local to your computer**.

You can use LockBytes to:

* 🔐 Encrypt sensitive files
* 🔓 Decrypt protected files
* 💾 Store vault information on a registered USB device
* 🛡️ Protect access using separate security credentials
* ☁️ Optionally synchronize recovery/backup information
* 📁 Work with LockBytes `.buri` protected files
* 🔄 Maintain vault synchronization and integrity information

### 🌐 Internet is NOT required for normal use

LockBytes does **not** require an internet connection for:

* File encryption
* File decryption
* Local vault access
* The main desktop application
* Working with locally available protected files

Internet connectivity may only be required for optional features such as:

* Recovery/backup synchronization
* Application update checks
* Other features that explicitly depend on an online service

---

# ✨ Features

## 🔐 Strong File Encryption

LockBytes uses modern cryptographic primitives to protect your files.

### AES-256-GCM

Files are protected using **AES-256-GCM authenticated encryption**, providing both confidentiality and integrity protection.

### Argon2id

Passwords are processed using **Argon2id-based key derivation**, designed to make password-based attacks significantly more expensive.

### Integrity Protection

Authenticated encryption helps LockBytes detect:

* Unauthorized modification
* Corrupted encrypted data
* Invalid authentication data

### Chunk-Based Processing

LockBytes uses chunk-based file processing to support workflows involving larger files without requiring the entire file to be handled as one in-memory object.

---

# 💾 USB-Based Vault

LockBytes uses a registered USB storage device as an important part of its vault security model.

The USB device can contain the vault-related information required by LockBytes to access protected vault data.

### Vault security includes:

* 🔑 Vault credentials
* 💾 Registered USB device
* 🔐 Cryptographic key derivation
* 🗂️ Vault metadata
* 🔄 Synchronization information
* 🛡️ Integrity-related security information

The USB device should be treated as an important security component of your LockBytes setup.

> **Keep your registered USB device safe.**

---

# 🔑 Multiple Security Layers

LockBytes separates security credentials for different purposes.

Depending on your configuration, this can include:

| Security Component       | Purpose                                         |
| ------------------------ | ----------------------------------------------- |
| 🔐 Vault Password        | Protects vault-related access                   |
| 🔒 App Lock Password     | Protects access to the application              |
| 🛡️ Recovery Credentials | Used for configured recovery workflows          |
| 💾 Registered USB        | Provides the required USB-based vault component |

This separation helps avoid relying on a single credential for every part of the application.

---

# ☁️ Optional Recovery & Backup

LockBytes can optionally connect to the user's **Google account** for recovery-related backup synchronization.

Recovery is completely optional.

You can use LockBytes normally without connecting a cloud account.

### Recovery features may include:

* ☁️ Recovery synchronization
* 💾 Encrypted backup information
* 🔄 Vault synchronization
* 🛡️ Recovery using configured credentials
* 📦 Backup of supported encrypted data

### Important

Google Drive is a third-party service and is subject to its own:

* Availability
* Terms
* Policies
* Account security requirements

LockBytes does not require Google Drive for normal local encryption and decryption.

---

# 📁 `.buri` Protected Files

LockBytes uses its own protected file format:

```text
.buri
```

When file association is enabled during installation, `.buri` files can be associated with LockBytes and opened through the application.

Example:

```text
personal-photo.jpg
        ↓
    LockBytes
        ↓
personal-photo.jpg.buri
```

The `.buri` file represents protected data and should **not be manually modified**.

---

# 🔄 Vault Synchronization & Integrity

LockBytes includes mechanisms designed to help maintain consistency between:

* Local vault information
* Vault metadata
* Recovery/backup information
* Synchronization state

These mechanisms are intended to help identify inconsistencies and maintain reliable vault state across supported workflows.

---

# 🖥️ Designed for Windows

LockBytes is currently designed for Windows desktop environments.

### Supported

* Windows 10
* Windows 11
* 64-bit Windows recommended

### Hardware

You will need:

* A Windows computer
* Sufficient local storage
* A USB storage device for USB-based vault functionality

---

# 📸 Screenshots

<p align="center">
  <img src="screenshots/dashboard.png" alt="LockBytes Dashboard" width="800">
</p>

<p align="center">
  <b>LockBytes Dashboard</b>
</p>

<br>

<p align="center">
  <img src="screenshots/vault.png" alt="LockBytes Vault" width="800">
</p>

<p align="center">
  <b>USB-Based Vault</b>
</p>

> **Note:** Place your actual screenshots inside a `screenshots` folder in the repository and update the filenames above if necessary.

---

# 🚀 Installation

## 1. Download LockBytes

Download the latest Windows installer from the **Releases** section.

### Recommended installer

```text
LockBytes-Setup-1.0.0.exe
```

The installer provides:

* Guided installation
* Start Menu shortcut
* Optional Desktop shortcut
* Application icon
* Optional `.buri` file association
* Uninstaller
* Application installation management
* Option to launch LockBytes after installation

---

## 2. Install LockBytes

Run:

```text
LockBytes-Setup-1.0.0.exe
```

Follow the installation wizard to complete the setup.

---

# ⚠️ Windows Security Warning

### LockBytes is currently not digitally code-signed.

Because the current Windows executable is not signed with a trusted code-signing certificate, Windows may display a warning when starting the installer.

You may see:

> **Windows protected your PC**

This warning can appear for independently distributed Windows applications that do not have trusted publisher verification.

### If you downloaded LockBytes from the official GitHub release:

1. Start the LockBytes installer.
2. If Windows displays the warning, select **More info**.
3. Review the application and publisher information.
4. If you trust the downloaded release, select **Run anyway**.
5. Continue with the installation.

After installation, you normally will not need to repeat this process every time you launch the application.

### ⚠️ Stay safe

Only bypass the Windows warning when you have downloaded LockBytes from a source you trust and have verified that the installer corresponds to the expected release.

A future release may include a trusted digital code-signing certificate for stronger publisher verification.

---

# 🛡️ Security Recommendations

LockBytes is designed to protect your files, but **security also depends on how you manage your credentials and devices**.

Before protecting important data:

### 🔑 Protect your credentials

Keep your:

* Vault Password
* App Lock Password
* Recovery information
* PRC / VRC information

in a safe location.

### 💾 Protect your USB device

Your registered USB device is an important component of the LockBytes vault system.

Do not:

* Lose the device
* Randomly modify LockBytes files
* Delete vault-related files
* Format the device without understanding the consequences

### 📦 Keep independent backups

LockBytes should **not be your only copy of important data**.

For critical files, maintain an independent backup in a secure location.

---

# 🚨 Important Data Recovery Warning

Encryption is intentionally designed so that unauthorized users cannot simply recover protected information.

That also means:

> **If required credentials or recovery material are permanently lost, your encrypted data may become permanently inaccessible.**

Do not rely on memory alone for important recovery information.

Store recovery information securely and separately from your primary device when appropriate.

---

# 🔒 Security Limitations

No security software can protect against every possible threat.

LockBytes may not protect your data from situations such as:

* Malware already present on the computer
* Keyloggers
* Compromised operating systems
* Hardware failure
* USB device failure
* Accidental deletion
* Lost credentials
* Compromised online accounts
* Physical access to an unlocked computer
* Other external security threats

LockBytes should therefore be considered **one part of a broader security and backup strategy**.

---

# 🧠 Security Philosophy

LockBytes follows a simple principle:

> ### Keep sensitive data protected without making the cloud mandatory.

The application is designed around three core ideas:

```text
             ┌──────────────────────┐
             │       LOCKBYTES       │
             └──────────┬───────────┘
                        │
        ┌───────────────┼───────────────┐
        │               │               │
        ▼               ▼               ▼
    🔐 PRIVACY      💾 CONTROL      🛡️ SECURITY
        │               │               │
     Local-first     USB Vault      Strong Crypto
```

Your normal encryption workflow stays local.

Cloud functionality is optional.

---

# 📦 Release Information

## LockBytes v1.0.0

**First Production Release**

| Property     | Details             |
| ------------ | ------------------- |
| Version      | `1.0.0`             |
| Release Type | Production / Stable |
| Platform     | Windows             |
| Architecture | 64-bit              |
| Developer    | Rahul Gupta         |
| File Format  | `.buri`             |
| Release Date | May 22              |

### What's included

* AES-256-GCM encryption
* Argon2id password-based key derivation
* USB-based vault
* Multiple security credentials
* `.buri` protected file format
* Vault integrity mechanisms
* Vault synchronization
* Optional recovery/backup
* Google Drive recovery synchronization
* Offline-first operation
* Windows installer
* Optional `.buri` file association

---

# 📥 Download

### Latest Version

**LockBytes v1.0.0**

`LockBytes-Setup-1.0.0.exe`

👉 **[Download the latest release](https://github.com/CodageWithRahul/LockBytes/releases/latest)**

For previous versions and release notes, visit the **[GitHub Releases](https://github.com/CodageWithRahul/LockBytes/releases)** page.

---

# 🧑‍💻 Project

LockBytes is developed by **Rahul Gupta** under **CodageWithRahul**.

The project is focused on building a practical desktop security application that combines:

* Modern encryption
* USB-based security
* Local-first workflows
* Optional recovery
* Simple desktop UX

---

# 📜 License & Documentation

The LockBytes installer includes the applicable **License** and **Terms of Use**.

Please review the included documentation before using LockBytes to protect important or sensitive information.

---

# 🤝 Contributing

Contributions, suggestions, bug reports, and feedback are welcome.

If you find an issue or have an idea that could improve LockBytes, open an issue in the GitHub repository.

Before reporting a security-related issue publicly, consider using an appropriate private disclosure method if one is available.

---

# ⭐ Support the Project

If you find LockBytes useful:

⭐ Star the repository
🐛 Report bugs
💡 Suggest improvements
📢 Share the project
🔐 Help make secure file management easier

---

# 🙏 Thank You

Thank you for checking out **LockBytes**.

The goal of LockBytes is simple:

> **Give users a practical way to protect sensitive files while keeping control of their data.**

No unnecessary cloud dependency.

No complicated workflow.

Just a secure, local-first approach to protecting your files.

---

<p align="center">

## 🔐 LockBytes

### Secure your files. Keep control of your data.

**© 2026 Rahul Gupta. All rights reserved.**

</p>
