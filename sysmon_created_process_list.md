**Purpose** : Created unique process list 

**Log Source** : Windows / Sysmon

**Analysis Techniques** : Get-WinEvent @{logname="Microsoft-Windows-Sysmon/Operational";id=1} | %{$_.Properties[3].Value} | sort -unique

**More Info** 
* https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/event.aspx?eventid=90001
