# Export all (or some) of your Azure RBAC rules (also Account Adminitsrator and Service Administrator) 
This Script will export the Owners and the Service Admins for all subscriptions user has access to
Each Subscription will have a seperate CSV file 
> Subscription--{Subscription Name}.csv

There will also be a single CSV file with all RBAC permissions 
> Subscription--All-Roles.csv

If a group is set to be an owner, the members will be also expoted
> GroupMembers--{Group Name}.csv

The script should work locally and on Azure Shell

## Install required PowerShell modules if not already installed
### If on Windows 10+
   > Install the latest version of WMF 
   > https://www.microsoft.com/en-us/download/details.aspx?id=54616
   > Then run 'Install-Module PowerShellGet -Force'
### If on Windows previous to 10
   > Install PackageManagement modules
   > http://go.microsoft.com/fwlink/?LinkID=746217
   > Then run 'Install-Module PowerShellGet -Force'

## If you want to export other RBAC rules or all of them:
You will need to search for the following line in the script:
```
$Current = Get-AzureRmRoleAssignment
```
and modify it as needed.

### Feel free to open a pull request if you like to improve this script
