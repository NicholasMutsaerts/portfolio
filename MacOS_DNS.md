---
layout: default
title: "IT Help Desk Guides"        # override site.title
description: "Improve DNS Performance on macOS"  # override site.description

---

### A Simple Guide to Updating DNS Settings on macOS

The Domain Name System (DNS) helps your Mac connect to websites faster by translating website names into IP addresses. Switching to a faster DNS provider can improve browsing speed, reliability, and security.

> **Note:** Apple may update menu layouts or features in future macOS versions. At the time of writing, the latest version is macOS 14 Sonoma.

---

### Step 1: Open Network Settings

1. Click the **Apple Menu**  in the top-left corner.
2. Select **System Settings**.
3. In the sidebar, click **Network**.

> You may need to scroll down to locate the Network option.

---

### Step 2: Select Your Network Connection

1. Choose the network service you are currently using:
   - Wi-Fi
   - Ethernet
2. Click **Details** beside the selected connection.

---

### Step 3: Open DNS Settings

1. In the settings window, click **DNS**.
2. Under **DNS Servers**, click the **"+" (Add)** button.
3. Enter the DNS server addresses you want to use.

You can add:
- IPv4 addresses
- IPv6 addresses

---

### Recommended DNS Providers

#### Google Public DNS

| Type | DNS Addresses |
|------|----------------|
| IPv4 | 8.8.8.8 and 8.8.4.4 |
| IPv6 | 2001:4860:4860::8888 and 2001:4860:4860::8844 |

---

#### Cloudflare DNS

| Type | DNS Addresses |
|------|----------------|
| IPv4 | 1.1.1.1 and 1.0.0.1 |
| IPv6 | 2606:4700:4700::1111 and 2606:4700:4700::1001 |

---

#### OpenDNS

| Type | DNS Addresses |
|------|----------------|
| IPv4 | 208.67.222.222 and 208.67.220.220 |
| IPv6 | 2620:119:35::35 and 2620:119:53::53 |

---

### Example Configuration

In this example, Google DNS servers were added to the DNS Servers list.

During this process, macOS may prompt you for:
- Administrator username
- Administrator password

This is required to authorize system-level network changes.

---

### Final Step

1. After entering the DNS addresses, click **OK**.
2. Close the settings window.

Your Mac will now use the new DNS servers.

---

### Benefits of Faster DNS Servers

- ✅ Faster website loading
- ✅ Improved browsing reliability
- ✅ Better security and privacy
- ✅ Reduced connection delays

---

### Quick Recommendation

| Best For | Recommended DNS |
|----------|-----------------|
| Speed & Privacy | Cloudflare DNS |
| Reliability | Google Public DNS |
| Content Filtering | OpenDNS |



