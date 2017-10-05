**Purpose** : Find hash data for each created process

**Log Source** : Windows / Sysmon

**Analysis Techniques** : Get-WinEvent  @{logname="Microsoft-Windows-Sysmon/Operational";id=1} | %{$_.Properties[11].Value}| sort -Unique

**More Info** 
* https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/event.aspx?eventid=90001
