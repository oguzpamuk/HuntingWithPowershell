**Purpose** : Identifying the names of users with login

**Log Source** : Windows / Security

**Analysis Techniques** : Get-WinEvent @{logname="security";id=4624} | {$_.Properties[5].Value} | sort -Unique

**More Info** 
* https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/event.aspx?eventid=4624
