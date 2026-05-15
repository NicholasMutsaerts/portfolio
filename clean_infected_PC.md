---
layout: default
title: "IT Help Desk Guides"        # override site.title
description: "Cleaning an infected PC"  # override site.description

---

Malware infections remain one of the most common and disruptive incidents faced by IT support teams. A successful cleanup requires a structured and methodical approach to fully remove threats and restore system integrity. 

This guide provides a practical, step‑by‑step approach to safely cleaning an infected Windows 11 system.

---
### 1. Disconnect from the Internet
Immediately disconnect the PC from the network (Ethernet & Wi-Fi) to prevent lateral movement or additional payload downloads.

### 2. Boot into Safe Mode
Safe Mode loads only essential drivers, making malware easier to detect and remove: Shift + Restart → Troubleshoot → Advanced Options → Startup Settings → F5

### 3. Verify System Integrity
Run System File Checker to repair corrupted Windows files within Command Prompt (Run as Administrator)

**sfc /scannow**

### 4. Run an Offline Malware Scan
Use Microsoft Defender Offline Scan to detect deeply embedded threats that evade live protection:

Windows Security → Virus & Threat Protection → Scan options

### 5. Clear Temporary Files
Remove files from temp. Press Windows + R, type temp, %temp%, and prefetch to speed up scans and eliminate hidden scripts. This process can help speed up scanning and may remove malicious scripts.

### 6. Review Startup Items
Check Task Manager → Startup and disable unknown or suspicious entries.

### 7. Secure Web Browsers
Remove malicious extensions
Reset browser settings (Chrome, Edge, Firefox)

### 8. Update Windows and All Software
Procced to fully update:

- Windows
- Antivirus definitions
- Browsers and third-party software

### 9. Rotate Credentials
After cleanup, change all critical passwords (email, banking, admin accounts). Use a password manager like Bitwarden or LastPass, and enable MFA.

### 10. Back Up Data (if Not Done Already)
Once confirmed clean, back up critical files to external or cloud storage.

---

### Last Resort
If malware persists or rootkits are suspected:

- [Reset This PC](https://support.microsoft.com/en-us/windows/reset-your-pc-0ef73740-b927-549b-b7c9-e6f2b48d275e)
- Or perform a clean Windows reinstall using the [Media Creation Tool](https://support.microsoft.com/en-us/windows/create-installation-media-for-windows-99a58364-8c02-206f-aa6f-40c3b507420d). Read: [Before you start the reinstall](https://support.microsoft.com/en-us/windows/reinstall-windows-with-the-installation-media-d8369486-3e33-7d9c-dccc-859e2b022fc7).

---

### Final Takeaway 
Successfully cleaning an infected Windows PC requires more than running a single antivirus scan. It demands a structured approach that prioritizes containment, thorough detection, system repair, and ongoing security best practices. For novice users and office staff, always escalate to your IT or security team.

---

#### [Go to the Home Page](/)
