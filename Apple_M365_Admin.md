---
layout: default
title: IT Technical Support Guides
description: Managing Microsoft 365 from MacOS
---

### Introduction

Microsoft 365 administration is no longer limited to Windows desktops. System administrators can successfully manage Microsoft 365 services such as Exchange Online, Azure Active Directory, Teams, and SharePoint from macOS. Microsoft 365 ecosystem support macOS for most administrative workflows, incuding:

- Microsoft 365 Admin Center (web-based)
- Exchange Admin Center (EAC)
- Microsoft Entra (Azure AD) admin portal
- PowerShell automation for advanced tasks

This article walks you through how to use macOS as your primary M365 admin workstation, focusing on installing PowerShell and connecting to Exchange Online.

---
### Why Use macOS for M365 Administration?

macOS is fully viable for M365 admins due to:

- Web-first management portals
- Cross-platform PowerShell (PowerShell 7+)
- Modern authentication support (including MFA)
- REST-based Exchange Online module (EXO V3)

Microsoft’s Exchange Online PowerShell module now supports macOS and Linux, enabling admin tasks without requiring Windows.

---

### Core Admin Tools on macOS
**1. Browser-Based Portals**
Most admin tasks can be done directly in a browser:

- Microsoft 365 Admin Center
- Exchange Admin Center
- Microsoft Entra Admin Center

These interfaces handle:

- User and license management
- Mailbox settings
- Security policies
- Device compliance

---

**2. PowerShell for Advanced Management**

PowerShell remains essential for:

- Bulk operations (mass mailbox updates)
- Automation scripts
- Advanced settings not exposed in UI

[Exchange Online PowerShell](https://learn.microsoft.com/en-us/powershell/exchange/exchange-online-powershell?view=exchange-ps) provides command-line access for managing mailboxes, rules, and organizational settings.

---
### System Requirements

Recommended requirements:

| Component | Recommendation |
|---|---|
| macOS Version | macOS Ventura or newer |
| RAM | 8 GB minimum |
| Storage | 30 GB free space |
| Browser | Safari, Chrome, or Edge |
| Permissions | Local administrator access |

---
### Requirements Checklist

Before connecting, ensure:

- PowerShell 7+ installed
- ExchangeOnlineManagement module installed
- Microsoft 365 admin account (Exchange Admin or Global Admin)
- Internet access (HTTPS port 443)
- PowerShellGet module available

These prerequisites are required for Exchange Online PowerShell sessions.

---

### Installing PowerShell on macOS

PowerShell 7+ is required for macOS

**Option 1: Install via Homebrew (recommended)**

**brew install powershell**

**Option 2: Install via Microsoft packages**

Download the latest PowerShell release from GitHub and install it manually. PowerShell 7.4 or later is recommended for macOS environments.

Verify installation

**pwsh
$PSVersionTable**

---

Installing Exchange Online PowerShell Module
The required module is ExchangeOnlineManagement (EXO V3).

**Install-Module -Name ExchangeOnlineManagement**

- Accept prompts (type Y)
- Installs from PowerShell Gallery

This module enables secure, modern authentication and supports MFA

**Verify Installation**

Get-Module ExchangeOnlineManagement -ListAvailable

**Import Module (optional)**

Import-Module ExchangeOnlineManagement

---

### Connecting to Exchange Online

**Basic Connection (Interactive Login)**

Connect-ExchangeOnline -UserPrincipalName admin@yourdomain.com

- Opens browser login
- Supports MFA
- Establishes session with Exchange Online

This uses modern authentication and works across platforms.

---

### Disconnecting Session
Always close sessions after use:

Disconnect-ExchangeOnline

---

### Quick Command Reference

# Start PowerShell
pwsh

# Install EXO module
Install-Module ExchangeOnlineManagement

# Connect to Exchange Online
Connect-ExchangeOnline -UserPrincipalName admin@domain.com

# Run command
Get-Mailbox

# Disconnect
Disconnect-ExchangeOnline

---

### Conclusion

macOS is now a fully capable platform for Microsoft 365 administration. With PowerShell 7 and the ExchangeOnlineManagement module, administrators can perform advanced tasks without needing Windows.

While GUI-based tasks remain web-driven, PowerShell unlocks automation and scale—making macOS a powerful and flexible admin environment.




