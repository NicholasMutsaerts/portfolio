# Windows Device Reset & BitLocker Recovery Guide

Use this one-page guide to reset a Windows device and prepare it for re-enrollment through Windows Autopilot when Intune management is no longer available.

## Before You Begin

Confirm the device is still registered in **Windows Autopilot** and associated with **Microsoft Entra ID**. If the device no longer appears in Intune, use Windows Recovery Environment instead of an Intune-initiated reset.

## Reset the Device

Reset the device from Windows Recovery Environment. This method does not require the local administrator password.

1. At the Windows sign-in screen, hold **Shift**, then select **Power** → **Restart**.
2. Select **Troubleshoot** → **Reset this PC** → **Remove everything**.
3. Choose **Local reinstall**, or select **Cloud download** if available.
4. Allow the reset to finish and return to the Windows out-of-box experience.

The reset prepares the laptop for Autopilot provisioning during the next setup.

## Complete Re-Enrollment

- Connect the laptop to the internet.
- Confirm the Autopilot profile is applied during setup.
- Have the assigned user sign in when prompted.
- Verify Intune enrollment and policy sync after setup completes.

## Retrieve the BitLocker Recovery Key

If the recovery screen appears, locate the matching BitLocker recovery key before continuing.

### Primary Source: Microsoft Entra ID

1. Open the **Microsoft Entra admin center**.
2. Go to **Devices** → **All devices**.
3. Select the affected laptop.
4. Open **BitLocker keys** or **Recovery keys**, then copy the matching key.

### Alternate Source: Microsoft Intune

If the device record still exists, go to:

**Devices** → **Windows** → **[Device]** → **Recovery keys**
