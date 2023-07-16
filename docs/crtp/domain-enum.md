## Domain Enumeration

### Tools
1. PowerView
    * [https://github.com/PowerShellMafia/PowerSploit/blob/master/Recon/PowerView.ps1](https://github.com/PowerShellMafia/PowerSploit/blob/master/Recon/PowerView.ps1)
2. Active Directory Powershell Module 
    * [https://docs.microsoft.com/en-us/powershell/module/addsadministration/?view=win10-ps](https://docs.microsoft.com/en-us/powershell/module/addsadministration/?view=win10-ps)
    * [https://github.com/samratashok/ADModule](https://github.com/samratashok/ADModule)
    * Load the module first - 
        * `Import-Module .\Microsoft.ActiveDirectory.Management.d11`
        * `Import-Module .\ActiveDirectory\ActiveDirectory.psd1`

### Commands 

#### Get Current Domain
* `Get-NetDomain` - PowerView
* `Get-ADDomain` - AD Powershell

#### Get Object of Another Domain
* `Get-NetDomain -Domain moneycorp.local`
* `Get-ADDomain -Identity moneycorp.local`

#### Get Domain SID for the current Domain
* `Get-DomainSID`
* `(Get-ADDomain).DomainSID`