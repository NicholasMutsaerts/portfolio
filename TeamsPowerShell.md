---
layout: default
title: "Mastering Microsoft Teams Administration with PowerShell"        # override site.title
description: ""  # override site.description
---

As Microsoft Teams continues to evolve as a core collaboration tool in modern workplaces, IT administrators are constantly seeking efficient methods to manage Teams at scale. Let us delve into the essential steps to get started.

Prerequisites: The first required steps lie in installing PowerShell 5.1 on Windows or PowerShell 7.2+ on all platforms. Install the [latest version of PowerShell](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell) available for your operating system.
Microsoft offers great resources for help desk support and system administrators:

•	[Microsoft Teams PowerShell Overview](https://lnkd.in/gZrkPr_U)
•	[Microsoft Teams PowerShell](https://lnkd.in/guKHNncH)
•	[Manage Teams with Microsoft Teams PowerShell](https://lnkd.in/gxAJY63X)

PowerShell is a game-changer for managing Microsoft Teams at scale. Here is an introductory cheatsheet. Please note that this list is not exhaustive, and for more in-depth information, you can refer to the embedded links below.

| Task / Description                                   | PowerShell Command(s)                                   |
|------------------------------------------------------|----------------------------------------------------------|
| Connect to Microsoft Teams PowerShell                | `Connect-MicrosoftTeams`                                |
| Get help and view Teams PowerShell cmdlets           | `Get-Help`, `Get-Help *MicrosoftTeams*`                 |
| List all Teams in the organization                   | `Get-Team`                                              |
| Create a new Team                                    | `New-Team`                                              |
| Add users to a Team                                  | `Add-TeamMember`                                        |
| Manage channels within a Team                        | `Get-Channel`, `New-Channel`                            |
| Manage Teams app policies and settings               | `Get-CsTeamsAppPolicy`, `Set-CsTeamsAppPolicy`          |

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
### External Source Links:

•	[Microsoft Teams PowerShell Overview](https://learn.microsoft.com/en-us/microsoftteams/teams-powershell-overview)
•	[Microsoft Teams PowerShell](https://learn.microsoft.com/en-us/microsoftteams/teams-powershell-install)
•	[Manage Teams with Microsoft Teams PowerShell](https://learn.microsoft.com/en-us/microsoftteams/teams-powershell-managing-teams)
•	[Get-CsTeamsAIPolicy](https://learn.microsoft.com/en-us/powershell/module/teams/get-csteamsaipolicy?view=teams-ps)
•	[Set-CsTeamsAIPolicy](https://learn.microsoft.com/en-us/powershell/module/teams/set-csteamsaipolicy?view=teams-ps)
•	[New-CsTEamsAIPolicy](https://learn.microsoft.com/en-us/powershell/module/teams/new-csteamsaipolicy?view=teams-ps)
•	[New-Team](https://learn.microsoft.com/en-us/powershell/module/teams/new-team?view=teams-ps)
•	[Add-TeamUser](https://learn.microsoft.com/en-us/powershell/module/teams/add-teamuser?view=teams-ps)

 

---
#### [IT Technical Support Guides](it-guides.md)
#### [Go to the Home Page]({{ '/' | absolute_url }})
