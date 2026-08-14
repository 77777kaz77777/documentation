Moving from Linux to Windows can feel like learning a new dialect[cite: 24]. While **CMD** is the "old guard" (legacy), **PowerShell** is the modern, object-oriented powerhouse that actually shares many aliases with Linux[cite: 24].
## **💻 Windows Command Line Comparison**
This table covers the most common file and system navigation tasks[cite: 24].
|  |  |  |  |
| :- | :- | :- | :- |
| Action | CMD (Command Prompt) | PowerShell | Linux (Reference) |
| **List Files** | dir[cite: 24] | ls or dir[cite: 24] | ls[cite: 24] |
| **Change Directory** | cd [folder][cite: 24] | cd [folder][cite: 24] | cd[cite: 24] |
| **Make Directory** | mkdir [name][cite: 24] | mkdir or md[cite: 24] | mkdir[cite: 24] |
| **Move/Rename** | move [src] [dest][cite: 24] | mv or Move-Item[cite: 24] | mv[cite: 24] |
| **Copy File** | copy [src] [dest][cite: 24] | cp or Copy-Item[cite: 24] | cp[cite: 24] |
| **Delete File** | del [file][cite: 24] | rm or Remove-Item[cite: 24] | rm[cite: 24] |
| **Clear Screen** | cls[cite: 24] | clear or cls[cite: 24] | clear[cite: 24] |
| **Show File Content** | type [file][cite: 24] | cat or Get-Content[cite: 24] | cat[cite: 24] |
| **Check IP Address** | ipconfig[cite: 24] | Get-NetIPAddress[cite: 24] | ip addr[cite: 24] |

## **🛠️ System & Networking**
In PowerShell, most commands follow a **Verb-Noun** structure (e.g., Get-Service), which makes them very predictable once you learn the pattern[cite: 24].
|  |  |  |
| :- | :- | :- |
| Action | CMD | PowerShell |
| **List Services** | sc query[cite: 24] | Get-Service[cite: 24] |
| **Stop Service** | net stop [name][cite: 24] | Stop-Service [name][cite: 24] |
| **List Running Apps** | tasklist[cite: 24] | Get-Process[cite: 24] |
| **Kill a Process** | taskkill /F /IM [app].exe[cite: 24] | Stop-Process -Name [app][cite: 24] |
| **Check Network Path** | tracert [url][cite: 24] | Test-NetConnection [url][cite: 24] |
| **Environment Vars** | set[cite: 24] | Get-ChildItem Env:[cite: 24] |

## **📦 Package Management (Winget)**
Windows now has a built-in package manager called **Winget**[cite: 24]. It works similarly to apt or dnf and is available in both CMD and PowerShell[cite: 24].
  - **Search for an app:** winget search [app_name][cite: 24]
  - **Install an app:** winget install [app_name][cite: 24]
  - **Update all apps:** winget upgrade --all[cite: 24]
  - **Uninstall an app:** winget uninstall [app_name][cite: 24]
## **💡 Pro Tips for your Google Doc**
  - **Administrator Access:** Many commands (like net stop or winget install) require you to run the terminal as an Administrator[cite: 24]. Right-click the Start button and select **Terminal (Admin)**[cite: 24].
  - **PowerShell Aliases:** PowerShell is designed to be friendly to Linux users[cite: 24]. It has "aliases" built-in, so ls, rm, and pwd work exactly as you’d expect without you needing to learn the long-form Windows commands immediately[cite: 24].
  - **The Pipeline:** In PowerShell, you aren't just passing text between commands like in Linux; you are passing **objects**[cite: 24]. This allows for much more powerful data filtering[cite: 24].
**Ready to paste?** When you bring this into your Google Doc, the tables will remain editable so you can add your own notes or frequently used server paths[cite: 24].
Would you like me to add a section on **Windows Registry** commands or **Active Directory** management for PowerShell?[cite: 24]
