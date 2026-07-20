# Windows 11: Create Standard and Administrator Users

*Quick guide using Computer Management*

> **## Open Computer Management> **Note:** Local Users and Groups is available in Windows 11 Pro, Enterprise, and Education. If you do not see it, use **Settings > Accounts > Other users** instead.

1. Right-click **Start** and select **Computer Management**.
2. Go to **System Tools > Local Users and Groups > Users**.

## Create a Standard User

1. In **Users**, right-click a blank area and select **New User**.
2. Enter the username and password.
3. Set password options as needed.
4. Click **Create**.

**Result:** The account is a standard user by default because it is only a member of the **Users** group.

## Create an Administrator User

1. Create the user using the steps above.
2. Double-click the account and open the **Member Of** tab.
3. Click **Add**, type **Administrators**, then click **Check Names**.
4. Click **OK**, **Apply**, and **OK**.

**Result:** The account now has local administrator privileges.

## Alternative: Make an Existing User an Administrator

1. Go to **Local Users and Groups > Groups**.
2. Double-click **Administrators**.
3. Click **Add**, enter the username, then click **Check Names** and **OK**.

## Verify Administrator Membership

Open Command Prompt as Administrator and run:

```cmd
net localgroup administrators

## Purpose

Local Windows accounts can be useful for users who do not have a Microsoft 365 or Entra ID account, but they should be used sparingly in an Intune-managed environment.

**Use cases include:**

- Temporary access for contractors, vendors, or short-term support.
- Offline or emergency sign-in when cloud access is unavailable.
- Kiosk, shared-use, or limited-purpose devices.
- Controlled break-glass access for IT recovery.

**Use caution because:**

- Local accounts are harder to manage, audit, and remove centrally.
- Conditional Access, MFA, and identity-risk policies may not apply the same way.
- Local passwords must be managed securely, ideally with Windows LAPS in Intune.

**Best practice:** Use Microsoft 365 or Entra ID accounts for regular users. Use local accounts only for specific support, kiosk, emergency, or shared-device scenarios. Avoid shared passwords and manage local admin credentials with Windows LAPS.

