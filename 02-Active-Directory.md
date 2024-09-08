# CHAPTER 2: ACTIVE DIRECTORY

1. Some note about Active Directory Domain Service (ADDS)
- You coul install DNS serice and global catalog (GC) on that domain controller server 

- Data folder and Log file of Domain controller store at path ``C:\Windows\NTDS`` and  Sysvol folder ``C:\Windows\SYSVOL``

- Powershell command line used to install ADDS service, aim upgrade windows server core upto domain controller.
```
powershell.exe
cd C:\
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
Install-ADDSForest -DomainName <ten_mien> 
```

2. Install Additional domain controller

- Prgress similar with install Domain controller, but chose ``Add domain controller to an existing domain``

3. Installing Child Domain

- At the ``Deployment configuration`` page, click ``Add a new domain to existing forest`` then specify new child domain name which you want. And choosing the ``Domain type`` is child domain, ``parent domain`` coressponding.

![child domain](https://github.com/hassj/MCSA/blob/main/image/01-Child-domain.JPG)

4. Creating User and group on Active DIRECTORY

![OU and Groups](https://github.com/hassj/MCSA/blob/main/image/01-User-group.JPG)

- Server Manager -> Actice Directory User and Computer -> New OU /Group/User (Group scope: Global; Group type: Security)

5. Creating OU on Active Directory

![OU and Groups](https://github.com/hassj/MCSA/blob/main/image/01-OU.JPG)

6. Delegate control to specific User

Click on OU/Group (which you want) -> choose delegate control -> select permission which you want -> next till finish

> Notice: RSAT - Remote Server Administration tools used to control and manage controller server with administrator privilege.

