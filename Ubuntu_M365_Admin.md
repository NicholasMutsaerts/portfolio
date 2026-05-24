---
layout: default
title: IT Technical Support Guides
description: Managing Microsoft 365 from Ubuntu
---

### Introduction

While Microsoft 365 (M365) administration is traditionally performed from Windows, modern tooling allows administrators to manage their tenant from **Ubuntu Linux** effectively.

With PowerShell 7 (cross-platform) and cloud-native tools, Ubuntu can serve as a lightweight, secure, and flexible admin workstation for:

- Exchange Online management
- Automation scripts
- Bulk operations
- Remote administration

Access to Microsoft 365 services from Linux is typically done through web apps or cross-platform tools since there is no full native desktop suite.

---

### Why Use Ubuntu for M365 Administration?
Using Ubuntu for Microsoft 365 administration offers several advantages:

**Benefits**

- **Cross-platform scripting** — run the same scripts on Linux, Windows, and macOS
- **Lightweight and fast** — minimal resource usage
- **Enhanced automation** — ideal for DevOps and scripting workflows
- **Security-focused** — open-source ecosystem with strong update practices

PowerShell provides a powerful command-line interface that allows administrators to automate tasks and manage cloud services efficiently.

---

### Step 1: Install PowerShell on Ubuntu
PowerShell 7 is the foundation for managing Microsoft 365 from Linux.

**Install via Microsoft Repository**

# Update packages
sudo apt-get update

# Install prerequisites
sudo apt-get install -y wget apt-transport-https software-properties-common

# Download Microsoft repository
wget -q https://packages.microsoft.com/config/ubuntu/$VERSION_ID/packages-microsoft-prod.deb

# Register repository
sudo dpkg -i packages-microsoft-prod.deb

# Update and install PowerShell
sudo apt-get update
sudo apt-get install -y powershell

# Launch PowerShell
pwsh

Microsoft recommends installing PowerShell via its package repository using APT for easier updates and management

**Verify Installation**

$PSVersionTable

You should see PowerShell 7.x.

---

### Step 2: Install Exchange Online PowerShell Module

The ExchangeOnlineManagement module is required to administer Exchange Online.

**Install Module**

Install-Module -Name ExchangeOnlineManagement -Scope CurrentUser

- Installs from the PowerShell Gallery
- Supports modern authentication and MFA
- Required for all Exchange Online connections

The ExchangeOnlineManagement module is the official Microsoft module for managing Exchange Online via PowerShell. 

---

#### Verify Installation

Get-Module ExchangeOnlineManagement -ListAvailable

---

### Step 3: Connect to Exchange Online

Once the module is installed, you can authenticate and connect.

**Connect Using Modern Authentication (Recommended)**

PowerShellConnect-ExchangeOnline -UserPrincipalName admin@yourdomain.comShow more lines

- Opens a browser for login
- Supports Multi-Factor Authentication
- Uses secure modern authentication

After authentication, all Exchange cmdlets become available.Connection requires PowerShell and proper admin permissions with outbound HTTPS access.

---

### Step 4: Common Administrative Tasks
Once connected, you can perform many tasks similar to Windows environments.

#### Example Tasks

**List Mailboxes**
PowerShellGet-MailboxShow more lines

**Create a Mailbox**
PowerShellNew-Mailbox -Name "John Doe" -UserPrincipalName john@domain.comShow more lines

**Set Mailbox Permissions**

PowerShellAdd-MailboxPermission -Identity user@domain.com -User admin@domain.com -AccessRights FullAccessShow more lines
PowerShell enables automation and bulk operations such as mailbox creation, permission assignment, and reporting.

---

### Step 5: Disconnect Session

Disconnect-ExchangeOnline

---

### Using Ubuntu for Full M365 Administration

While PowerShell covers Exchange Online, other services are typically managed via:

**Web Interfaces***

- Microsoft 365 Admin Center
- Azure Portal
- Exchange Admin Center

Linux users typically access M365 primarily via browser-based tools alongside scripting utilities.

---

### Conclusion

Ubuntu is a **fully capable platform for Microsoft 365 administration**, especially when combined with PowerShell 7 and modern modules.
With this setup, you can:

- Manage Exchange Online
- Automate administrative workflows
- Operate cross-platform admin environments

PowerShell and cloud-native tools make Windows no longer a strict requirement for M365 administration tasks.


