---
layout: default
title: "IT Help Desk Guides"        # override site.title
description: "Temporary Access Pass (TAP) Guide"  # override site.description

---

# Microsoft 365 Admin Guide: Temporary Access Pass (TAP)
Secure First-Time Sign-In & Passwordless Onboarding

---

## Overview
Temporary Access Pass (TAP) is a **time-limited** passcode issued by administrators that allows users to securely sign in and register authentication methods without requiring a preconfigured password. TAP supports secure onboarding and passwordless scenarios by providing short-term, controlled access.

---

## Common Use Cases
- New employee onboarding  
- Passwordless deployments  
- Device provisioning with Windows Autopilot  
- MFA recovery scenarios  
- Secure remote setup  

---

## Enable the Temporary Access Pass Policy

### Prerequisite
You must have the [Authentication Policy Administrator](https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/permissions-reference) role to update the TAP authentication methods policy.

### Steps
1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com/)  
2. Navigate to:  
   **Microsoft Entra ID → Authentication methods → Policies**  
3. From the list, select **Temporary Access Pass**  
4. Select **Enable** and define target users (include/exclude)  
5. (Optional) Select **Configure** to adjust:
   - Maximum lifetime  
   - Pass length  
6. Select **Save** to apply the policy  

---

## Create a Temporary Access Pass (Admin Steps)

1. Open the Microsoft Entra Admin Center:  
   [https://entra.microsoft.com](https://entra.microsoft.com])  
2. Navigate:  
   **Identity → Users → Select User**  
3. Select:  
   **Authentication methods → Temporary Access Pass → Add**  

### Configuration Options
- One-time use  
- Lifetime: 1–8 hours  
- Activate immediately  
- Pass length: Default  

---

## User Sign-In Experience

1. Start device and connect to Wi-Fi  
2. Enter corporate email  
3. Select:  
   **Sign-in options → Temporary Access Pass**  
4. Enter TAP code  

### Complete Setup
- Create password  
- Register MFA  
- Device auto-enrolls in Intune  

---

## Best Practices
- Use TAP instead of temporary passwords  
- Keep TAP short-lived and one-time use  
- Deliver via a secure, separate channel  
- Ensure Intune + Autopilot are configured  
- Verify device enrollment  

---

## Security Considerations
- TAP is **not a password**  
- Expires automatically after use  
- Should never be reused or stored  
- Always enforce MFA registration  

---

## Sources
- https://learn.microsoft.com/en-us/entra/identity/authentication/howto-authentication-temporary-access-pass  
- https://techcommunity.microsoft.com/blog/itopstalkblog/step-by-step-guide--how-to-use-temporary-access-pass-tap-with-internal-guest-use/4365541























