**Purpose** : Determine who and when windows security logs are deleted

**Log Source** : Windows / Security

**Analysis Techniques** : Get-WinEvent @{logname="security";id=1102}

**More Info** 
* https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/event.aspx?eventid=1102
