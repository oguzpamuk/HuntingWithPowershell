**Purpose** : Identifying the names of users with failed login

**Log Source** : Windows / Security

**Analysis Techniques** : Get-WinEvent @{logname="security";id=4625} | %{$_.Properties[5].Value} | sort -Unique

**More Info** 
* https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/event.aspx?eventid=4625
