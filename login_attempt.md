**Purpose** : Determine who and when windows security logs are deleted

**Log Source** : Windows / Security

**Analysis Techniques** : Get-WinEvent -FilterHashtable @{logname="security";id=4776} | %{$_.Properties[1].Value} | sort -Unique

**4776 Details** :

| Error Code 	| Description                                                             	|
|------------	|-------------------------------------------------------------------------	|
| C0000064   	| user name does not exist                                                	|
| C000006A   	| user name is correct but the password is wrong                          	|
| C0000234   	| user is currently locked out                                            	|
| C0000072   	| account is currently disabled                                           	|
| C000006F   	| user tried to logon outside his day of week or time of day restrictions 	|
| C0000070   	| workstation restriction                                                 	|
| C0000193   	| account expiration                                                      	|
| C0000071   	| expired password                                                        	|
| C0000224   	| user is required to change password at next logon                       	|
| C0000225   	| evidently a bug in Windows and not a risk                               	|

**More Info** 
* https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/event.aspx?eventid=4776

