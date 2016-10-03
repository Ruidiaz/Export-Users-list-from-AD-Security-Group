# Export-Users-list-from-AD-Security-Group
How to export users list from AD security group in csv format

From Powershell...


      Import-Module ActiveDirectory
      Get-ADGroupMember -identity “Name of Group” | select name | Export-csv -path C:\temp\Groupmembers.csv -NoTypeInformation

*This will create a .csv named GroupMembers within C:\temp with a list of the users/members of the group.
** "Name of Group" is the Group name(pre-Windows 2000)
