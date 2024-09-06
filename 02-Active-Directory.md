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

![child domain](01-Child-domain.JPG)