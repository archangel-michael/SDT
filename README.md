# SDT
## Standard Desktop Tools`


|Description| Link|
|-----------|:-----|
|mRemoteNG|[Download](https://mremoteng.org/download)|
|Putty|[Download](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)|
|WinSCP|[Download](https://winscp.net/eng/download.php)|
|PomoDoneApp|[Download](https://pomodoneapp.com/)|
|Notepad++|[Download](https://notepad-plus-plus.org/download/)|
|VSCode|[Download](https://code.visualstudio.com/)|
|Windows AWS CLI|[Download](https://s3.amazonaws.com/aws-cli/AWSCLI64.msi)|
|AWS SDK for Python(Boto3)|pip install boto3|
|Xmind| [Download](https://www.xmind.net/download/)|
|Symantec VIP|[Download](https://vip.symantec.com/)|
|Draw. io| [Download](https://www.draw.io/)|
|VMWare Workstation Pro|[Download V14](https://my.vmware.com/en/web/vmware/info/slug/desktop_end_user_computing/vmware_workstation_pro/14_0) - [Key](https://mail.google.com/mail/u/0/#search/vmware/WhctKHScNkCSPrTMxJhwhMrXxWfrsQKbfJQtFcWpZQzQvMPWVwNLPJFCcRsMnTBSCzhkZBV) - Secondary Key - 2N61P-61H13-08LDN-0F8HM-1T01J|
|Evernote|[Download](https://evernote.com/download/?utm_campaign=engt_web_downloadLink_WEB-45641B_v1&utm_source=evernote&utm_medium=web)|
|Scrivener|[Download](https://www.literatureandlatte.com/scrivener/download) - [Key](https://mail.google.com/mail/u/0/#search/scrivener/DmwnWrRlQHQSlldJfRPlFVJWcZLglgzWhBCbSFTWQMwGfBzBlQKDpnhsgwTrnLMKMkcvzhkKlctl)|




### Coding Languages and tools
|Description| Link|
|-----------|:-----|
|Python|https://www.python.org/downloads/|
|GoLang|https://golang.org/dl/|
|GitHub|https://desktop.github.com/|
|SourceTree|https://www.sourcetreeapp.com/|


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
>regedit /i putty.reg

PowerShell:

>reg import putty-sessions.reg
>reg import putty.reg

>Note: do not replace SimonTatham with your username.

>Note: It will create a reg file on the Desktop of the current user.

>Note: It will not export related SSH keys.

