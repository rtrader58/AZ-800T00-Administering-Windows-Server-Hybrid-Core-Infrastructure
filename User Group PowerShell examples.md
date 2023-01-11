# User Group PowerShell examples

## Created by Janet Nichols

### Create a new user in the IT ou
New-ADUser -Name Macie -DisplayName "Macie Nichols" -GivenName Macie -Surname Nichols -Path "ou=it,dc=adatum,dc=com"

### Manually set a password
Set-ADAccountPassword Macie

### Enable the account
Enable-ADAccount Macie

### View the user
get-aduser macie

### create a new user in the IT ou and set a password and enable the account

New-ADUser "Ron" -AccountPassword (Read-Host -AsSecureString "Enter password") -Department IT -City London -surname Howard -givenname Ron -Path "ou=it,dc=adatum,dc=com" -enabled $true

### create a new global group 
New-ADGroup -Name "DesktopSupport" -Path "ou=it,dc=adatum,dc=com" -GroupScope Global -GroupCategory Security

### add new members to the global group
Add-Adgroupmember DesktopSupport Macie,abbi,ron

### view membership of the group
Get-ADGroupMember DesktopSupport

### formatting of the group members
get-adgroupmember helpdesk|select name|ft

### sets group description matching the criteria 
get-adgroup -filter {name -like "LonAdmins"}|set-adgroup -description "Managers of London ou"

### creates a new OU
New-ADOrganizationalUnit -Name FilePrint -Path "ou=servers,dc=adatum,dc=com" -passthru

### creates a new Computer
New-ADComputer -Name LON-SVR8 -Path "ou=fileprint,ou=servers,dc=adatum,dc=com" -Enabled $true

### Retrieves a list of users with the surname of Yoo
Get-ADUser -Filter {sn -eq "Yoo"}

### displays all users in and under the It ou in a gridview
Get-ADUser -Filter * -SearchBase "ou=it,dc=adatum,dc=com"|out-gridview

### List of users who last logged in before 1/1/2017
Get-ADUser -Filter {lastlogondate -lt "January 1, 2017"}

### List of users who last logged in before 1/1/2017 and disables their accounts
Get-ADUser -Filter {lastlogondate -lt "January 1, 2017"}| Disable-ADAccount

###  Retrieve all disabled user accounts
Search-ADAccount -AccountDisabled -UsersOnly

###  Retrieve all user accounts inactive for the last 5 days
Search-ADAccount -AccountInactive -TimeSpan -5 -UsersOnly|select name|ft

###  Retrieve all user accounts whose password will expire on 7/4/2016
Search-ADAccount -AccountExpiring -DateTime "1/1/2017" -UsersOnly

###  Retrieve all computer accounts that are locked out
Search-ADAccount -ComputersOnly -LockedOut