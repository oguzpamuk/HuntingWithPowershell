**Purpose** : Count of logins by username

**Log Source** : Windows / Security

**Analysis Techniques** : Get-WinEvent @{logname="security";id=4624} | %{$_.Properties[5].Value} | group-object -noelement | sort count

**More Info** 
* https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/event.aspx?eventid=4624
