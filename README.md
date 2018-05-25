# SDT
## Standard Desktop Tools`

### Session Management
|Description| Link|
|-----------|:-----|
|mRemoteNG|https://mremoteng.org/download|
|Putty|https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html|


### Editing Tools
|Description| Link|
|-----------|:-----|
|Notepad++|https://notepad-plus-plus.org/download/|
|VSCode|https://code.visualstudio.com/|


### Coding Languages and tools
|Description| Link|
|-----------|:-----|
|Python|https://www.python.org/downloads/|
|GoLang|https://golang.org/dl/|
|GitHub|https://desktop.github.com/|



# Notes, Tips and Tricks
## Export and Import putty configs 

### Export
**cmd.exe, require elevated prompt:**

>Only sessions:

>regedit /e "%USERPROFILE%\Desktop\putty-sessions.reg" HKEY_CURRENT_USER\Software\SimonTatham\PuTTY\Sessions

>All settings:

>regedit /e "%USERPROFILE%\Desktop\putty.reg" HKEY_CURRENT_USER\Software\SimonTatham

Powershell:

>Only sessions:

>reg export HKCU\Software\SimonTatham\PuTTY\Sessions ([Environment]::GetFolderPath("Desktop") + "\putty-sessions.reg")

>All settings:

>reg export HKCU\Software\SimonTatham ([Environment]::GetFolderPath("Desktop") + "\putty.reg")

### Import

>Double-click on the *.reg file and accept the import.
>Alternative ways:
>cmd.exe, require elevated command prompt:

>regedit /i putty-sessions.reg
regedit /i putty.reg

PowerShell:

>reg import putty-sessions.reg
>reg import putty.reg

>Note: do not replace SimonTatham with your username.

>Note: It will create a reg file on the Desktop of the current user.

>Note: It will not export related SSH keys.

