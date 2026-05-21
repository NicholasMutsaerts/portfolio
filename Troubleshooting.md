---
layout: default
title: "IT Help Desk Guides"        # override site.title
description: "Common IT Troubleshooting Scenarios for Windows 11"  # override site.description

---

This guide outlines common Windows 11 issues encountered in help desk and junior system administrator roles. As an IT professional or system administrator, understanding how to quickly diagnose and resolve these problems is essential. The focus is on practical troubleshooting steps for some of the most common Windows 11 support scenarios encountered in home and enterprise environments.

---

### Troubleshooting a computer that will not turn on

Start by checking the power source, cables, and outlet. Look for signs of power, such as lights or fans. Try a different power cable or outlet. If it powers on, but will not book, disconnect the peripherals and check hardware, like RAM.

---

### Slow System Performance 

Performance can suffer from excessive background applications or limited disk space. Constantly maintain your system by closing unused programs, clearing temporary files, and running disk cleanup. 

For Windows 11, proceed to disable startup add. Proceed to open Task Manager > Startup tab > Disable unneeded programs. 

Adjust Visual Effects: Go to System Properties → Advanced → Performance Settings → Select Adjust for best performance.

A refresh install of Windows 11 once a year can also help remove accumulated clutter and restore system stability.

---

### Checks the integrity of Windows file system

System File Checker (SFC) helps replace corrupted files with cached copies. Run this command via Command Prompt as Administrator

**sfc /scannow**

Deployment Imaging Service and Management Tool (DISM) is Used to fix Windows image and servicing problems. Run this command after SFC does not fix the issue. It connects to Windows Update to replace corrupted files

**DISM /Online /Cleanup-Image /RestoreHealth**

---

### Network and Internet Connectivity Problems

Restarting the router and checking if the device is connected to the right network. Verify the IP configuration. Basic troubleshooting for internet connectivity should include restarting the router and checking the cables. Determine if the issue is affecting one user or more.

In Windows 11, use the **netsh winsock reset** command when experiencing network connectivity issues that cannot be resolved through standard troubleshooting steps. 

A few common scenarios are malware infection, network configuration issues, and VPN issues. **Winsock reset** command restarts the communication required between your device and the network. (Run Command Prompt as Administrator).

1. Type **netsh winsock reset** and select **Enter**.
2. Type **netsh int ip reset** and select **Enter**.
3. Type **ipconfig /release** and select **Enter**.
4. Type **ipconfig /renew** and select **Enter**.
5. Type **ipconfig /flushdns** and select **Enter**.

If you experience persistent internet problems, go to **Settings > Network & Internet > Advanced network settings > Network reset**, then restart your computer.

Consider running an Internet speed test in order to verify upload and download speeds. Try [speedtest](https://www.speedtest.net/) and [internet speed test](https://fast.com/). A good internet speed for home use is 100 Mbps upload and download speed. For an office environment, the ideal internet speed will depend on the number of staff members in the office. 

---

### Forgotten Password

Password resets are a common tasks for helpdesk teams. Implementing self-service password reset tools can simplify this process and minimize downtime. Encourage users to enable two-factor authentication for enhanced security and use password managers to prevent forgotten passwords. Tools like [LastPass](https://www.lastpass.com/), [NordPass](https://nordpass.com/) and [Bitwarden](https://bitwarden.com/) are excellent options. 

---

### Microsoft Outlook Connectivity Issues

Proceed to verify connectivity, confirm Outlook is not in **Offline Mode**, manually run **Send/Receive**, Check Junk E-mail and deleted Items folder, check mailbox capacity, confirm account configuration, and restart & update. 

---

### Printer is not working

Network printer issues can be a daily concern for help desk teams. Here are a few troubleshooting steps. 

- Verify if the printer and the computer are connected to the right network. 
- Proceed to update printer drivers. In some occasions, remove and readd the printer.
- Check printer paper tray and toner levels. 
- Occasionally a computer restart can resolve the issue. 

For local printers, ensure that the printer cable is properly connected. Check out Microsoft Support for [Add or Install a Printer in Windows 11](https://support.microsoft.com/en-us/windows/add-or-install-a-printer-in-windows-cc0724cf-793e-3542-d1ff-727e4978638b) and [How to download and install the latest printer drivers](https://support.microsoft.com/en-us/windows/download-and-install-the-latest-printer-drivers-4ff66446-a2ab-b77f-46f4-a6d3fe4bf661). 

#### Restart the Print Spooler
1. Press **Win** + **R**
2. Type: **services.msc**
3. Locate **Print Spooler**
4. Restart the service

#### Clear the Print Queue
1. Open PowerShell and type in the following command line
   **C:\Windows\System32\spool\PRINTERS**
2. Delete pending print jobs

---

### Software Crashes or Freezes

Instruct the user to close and reopen the application or restart their computer. If the issue persists, proceed to assist with updating software updates or reinstalling the application. For Windows 11, consider updating drivers via Device Manager. Check out [How to install Windows Updates](https://support.microsoft.com/en-us/windows/install-windows-updates-3c5ae7fc-9fb6-9af1-1984-b5e0412c556a#:~:text=To%20check%20for%20updates%2C%20select,can%20choose%20to%20install%20them.&text=If%20you%20run%20into%20problems,at%20Troubleshoot%20problems%20updating%20Windows.). 

---

### How to setup MFA in Microsoft 365 Administration

**Short Answer:**
1. Sign in to Microsoft 365 Admin Center
2. Go to Users --> Active users
3. Select a user --> Manage multifactor authentication
4. Enable MFA for the user
5. User signs in and sets up MFA (Authenticator app, phone, etc.)

**Alternatively:** Use Microsoft Entra ID (Azure AD) --> Security --> Conditional Access to enforce MFA for all users. 

---

### How to setup Conditional Access

**Short Answer (Microsoft 365 / Entra ID)**
1.	Sign in to Microsoft Entra admin center
2.	Go to Security  Conditional Access
3.	Click + New Policy
4.	Choose Users (who it applies to)
5.	Choose Cloud apps (what it protects)
6.	Under Access controls, select Grant  Require multi-factor authentication
7.	Enable the policy and Save.

---

### Quick Fixes
- **Restart the computer:** A simple restart often resolves many temporary glitches and performance issues by refreshing system processes and clearing cached data.
- **Use troubleshooters:** Use troubleshooters: **Go to Settings > System > Troubleshoot > Other troubleshooters** to find and run automated tools for common problems like audio, network, or Windows Update issues. 
- **Install the latest updates**. To check for updates, select **Start > Settings > Windows Update**, then select Check for updates. 
- **Check Storage:** Be sure that you have at least 10-15% of free space on your hard drive, as a lack of space can cause performance issue. ou can free up space by running **Disk Cleanup** or navigating to **Settings > System > Storage > Cleanup recommendations** to remove temporary and unused files.
- **Update Device Drivers:** Outdated or incompatible drivers can lead to hardware malfunctions. Go to **Settings > Windows Update > Advanced options > Optional updates** and install any available driver updates, or use **Device Manager** to check manually.

---

### Microsoft PC Manager

**Microsoft PC Manager** is designed to be lightweight, user-friendly, and effective across a wide range of hardware configurations. It is now available for download via the [Microsoft Store](https://apps.microsoft.com/home?hl=en-GB&gl=CA). Key Features:

1. **One-Click Performance Boost:** Instantly enhance your PC's performance by cleaning up temporary files and optimizing memory usage. 
2. **Storage Optimization:** Reclaim storage space by organizing large files, uninstalling rarely used apps, and enabling storage sense to automatically clear temporary files. 
3. **File Organization:** Simplify file and folder management with user-friendly, built-in tools. 
4. **Enhanced Security:** Safeguard your default settings from unauthorized changes and perform threat scans with a single-click security check. 
5. **Pop-Up Control:** Minimize ads and app pop-ups for a seamless, distraction-free experience. 
6. **Comprehensive Health Check:** Detect and resolve system issues efficiently with an all-in-one health check.

--- 

### Using Ticketing Systems Effectively

Good troubleshooting lies within proper documentation and technical solutions. This process will be a big time saver for IT team for future tickets. Every ticket should include:

- Symptoms
- Root cause
- Steps taken
- Resolution

Help Desk work is about problem-solving, communication, and consistency. Master these common scenarios, and you’ll succeed in any IT support role.

**Final Tip:** Most issues can be solved faster by asking:

- When did it start?
- What changed?
- Does it affect other users?

---

### Final Thoughts

In IT helpdesk support, many technical issues can be resolved through quick and effective troubleshooting. Empowering users to address basic problems on their own not only speeds up resolution times but also creates a more efficient and proactive support environment. Building a well-structured knowledge base with clear, concise reference guides can significantly enhance incident management and overall help desk performance.



