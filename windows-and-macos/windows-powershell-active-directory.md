## **Windows PowerShell & Active Directory Essentials**
### **🗝️ Windows Registry Management**
In PowerShell, the Registry is treated like a file drive (HKLM: for HKEY_LOCAL_MACHINE and HKCU: for HKEY_CURRENT_USER)[cite: 21].
|  |  |
| :- | :- |
| Action | PowerShell Command |
| **Go to Registry Key** | cd HKLM:\Software\Microsoft[cite: 21] |
| **List Values in Key** | Get-ItemProperty -Path .[cite: 21] |
| **Create New Key** | New-Item -Path .\MyNewKey[cite: 21] |
| **Set/Change Value** | Set-ItemProperty -Path . -Name "Version" -Value "1.1"[cite: 21] |
| **Get Specific Value** | Get-ItemProperty -Path . -Name "Version"[cite: 21] |
| **Remove Key/Value** | Remove-ItemProperty or Remove-Item[cite: 21] |

### **👥 Active Directory (AD) Management**
*Note: These require the RSAT (Remote Server Administration Tools) to be installed on your machine[cite: 21].*
|  |  |
| :- | :- |
| Action | PowerShell Command |
| **Get User Info** | Get-ADUser -Identity [username] -Properties *[cite: 21] |
| **Create New User** | New-ADUser -Name "John Doe" -SamAccountName jdoe[cite: 21] |
| **Unlock Account** | Unlock-ADAccount -Identity [username][cite: 21] |
| **Reset Password** | Set-ADAccountPassword -Identity [username][cite: 21] |
| **Add to Group** | Add-ADGroupMember -Identity [Group] -Members [User][cite: 21] |
| **List Group Members** | Get-ADGroupMember -Identity [GroupName][cite: 21] |
| **Find Computers** | Get-ADComputer -Filter 'Name -like "*Desktop*"'[cite: 21] |

### **🛰️ Windows Networking & Remote Management**
PowerShell excels at managing remote Windows machines using **WinRM**[cite: 21].
  - **Enter a Remote Session:** Enter-PSSession -ComputerName [RemotePC] (Like SSH for Windows)[cite: 21].
  - **Run Command Remotely:** Invoke-Command -ComputerName [RemotePC] -ScriptBlock { Get-Service }[cite: 21]
  - **Test Network Port:** Test-NetConnection -ComputerName [IP] -Port 80 (A modern telnet replacement)[cite: 21].
### **📊 Comparing CMD vs. PowerShell Objects**
The biggest hurdle is realizing that PowerShell doesn't just return text; it returns **Data Objects**[cite: 21].
  - **Linux/CMD style (Text):** You grep or find a string of text[cite: 21].
  - **PowerShell style (Objects):** You filter by properties[cite: 21].
  - *Example:* Get-Service | Where-Object {$_.Status -eq "Running"} only shows services that are actually started[cite: 21].
Would you like me to create a dedicated section for **Azure CLI** or **Microsoft 365** PowerShell commands to round out your cloud administration toolkit?[cite: 21]
