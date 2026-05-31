---
layout: default
title: "IT Guides"        # override site.title
description: "Mastering Microsoft Teams Administration with PowerShell"  # override site.description
---

As Microsoft Teams continues to evolve as a core collaboration tool in modern workplaces, IT administrators are constantly seeking efficient methods to manage Teams at scale. Let us delve into the essential steps to get started.

**Prerequisites:** The first required steps lie in installing PowerShell 5.1 on Windows or PowerShell 7.2+ on all platforms. Install the [latest version of PowerShell](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell) available for your operating system.

Microsoft offers great resources for help desk support and system administrators:

- [Microsoft Teams PowerShell Overview](https://lnkd.in/gZrkPr_U)
- [Microsoft Teams PowerShell](https://lnkd.in/guKHNncH)
- [Manage Teams with Microsoft Teams PowerShell](https://lnkd.in/gxAJY63X)

---

### Why Use PowerShell for Microsoft Teams?

PowerShell enables administrators to:

- Automate repetitive administrative tasks.
- Manage Teams policies and settings at scale.
- Create and manage teams in bulk.
- Generate reports and audit configurations.
- Streamline user and policy management.

For organizations with large Teams deployments, PowerShell is an essential tool that improves efficiency, consistency, and administrative control.

---

### Common Teams PowerShell Commands

The following commands provide a starting point for managing Microsoft Teams environments:

| Task / Description                                   | PowerShell Command(s)                                   |
|------------------------------------------------------|----------------------------------------------------------|
| Connect to Microsoft Teams PowerShell                | `Connect-MicrosoftTeams`                                |
| Get help and view Teams PowerShell cmdlets           | `Get-Help`, `Get-Help *MicrosoftTeams*`                 |
| List all Teams in the organization                   | `Get-Team`                                              |
| Create a new Team                                    | `New-Team`                                              |
| Add users to a Team                                  | `Add-TeamMember`                                        |
| Manage channels within a Team                        | `Get-Channel`, `New-Channel`                            |
| Manage Teams app policies and settings               | `Get-CsTeamsAppPolicy`, `Set-CsTeamsAppPolicy`          |
| Remove a standard channel                            | `Remove-TeamsChannels -GroupID <TeamId> -Displayname "Channel Name"' |
| Remove a private channel                             |  Remove-TeamsChannels -GroupID <TeamId> -Displayname "Private Channel Name" - Force'  |

**Note:** This list represents only a small subset of the available Microsoft Teams PowerShell cmdlets. Administrators are encouraged to consult Microsoft's official documentation for comprehensive guidance and additional examples.

---
## Microsoft Teams AI Policies

Microsoft Teams includes AI capabilities such as facial recognition, voice enrollment, and speaker attribution.

### Teams AI Policy Commands

| Action | PowerShell Command | Description |
|------|-------------------|------------|
| Retrieve AI policies | `Get-CsTeamsAIPolicy` | Retrieves Teams AI policies and displays `EnrollFace`, `EnrollVoice`, and `SpeakerAttributionBYOD` values |
| Create a new policy | `New-CsTeamsAIPolicy -Identity Test` | Creates a new Teams AI policy with the specified identity |
| Remove a policy | `Remove-CsTeamsAIPolicy -Identity "Test"` | Deletes the Teams AI policy with the identity **Test** |
| Disable facial enrollment (Global) | `Set-CsTeamsAIPolicy -Identity Global -EnrollFace Disabled` | Disables facial enrollment globally |
| Enable voice enrollment (Test) | `Set-CsTeamsAIPolicy -Identity Test -EnrollVoice Enabled` | Enables voice enrollment for the **Test** policy |
| Disable speaker attribution (Global) | `Set-CsTeamsAIPolicy -Identity Global -SpeakerAttributionBYOD Disabled` | Disables speaker attribution for BYOD users globally |

---
### Teams AI Policy Attributes

| Attribute | Description |
|---------|-------------|
| `EnrollFace` | Enable or disable facial enrollment |
| `EnrollVoice` | Enable or disable voice enrollment |
| `SpeakerAttributionBYOD` | Attribution for BYOD (Bring Your Own Device) users |

---
### Team and User Management Basics

| PowerShell Command | Description |
|------------------|-------------|
| `New-Team -DisplayName "Project X Team"` | Creates a new team named **Project X Team** |
| `Add-TeamUser -GroupId <TeamID> -User <UserEmail>` | Adds a user to the specified team |

---

### Microsoft Teams PowerShell Quick Reference Infographic

[Microsoft Teams PowerShell Infographic (downloadable PDF)](pdf/Microsoft_Teams_PowerShell_Infographic.pdf)

---
### External Source Links:

-	[Microsoft Teams PowerShell Overview](https://learn.microsoft.com/en-us/microsoftteams/teams-powershell-overview)
-	[Microsoft Teams PowerShell](https://learn.microsoft.com/en-us/microsoftteams/teams-powershell-install)
-	[Manage Teams with Microsoft Teams PowerShell](https://learn.microsoft.com/en-us/microsoftteams/teams-powershell-managing-teams)
-	[Get-CsTeamsAIPolicy](https://learn.microsoft.com/en-us/powershell/module/teams/get-csteamsaipolicy?view=teams-ps)
-	[Set-CsTeamsAIPolicy](https://learn.microsoft.com/en-us/powershell/module/teams/set-csteamsaipolicy?view=teams-ps)
-	[New-CsTEamsAIPolicy](https://learn.microsoft.com/en-us/powershell/module/teams/new-csteamsaipolicy?view=teams-ps)
-	[New-Team](https://learn.microsoft.com/en-us/powershell/module/teams/new-team?view=teams-ps)
-	[Add-TeamUser](https://learn.microsoft.com/en-us/powershell/module/teams/add-teamuser?view=teams-ps)

---

### Conclusion:

Microsoft Teams PowerShell is a valuable tool for administrators who need to manage Teams efficiently and at scale. PowerShell provides the flexibility and automation capabilities required to support modern collaboration environments. Investing time in learning these cmdlets can significantly reduce administrative overhead and improve operational consistency across your Microsoft 365 tenant.
