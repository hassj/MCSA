# CHAPTER 3: POWER SHELL

## Chapter 3.1: Creating OU, User using powershell

- Creating OU

![Creating OU using Powershell](https://github.com/hassj/MCSA/blob/main/image/03-Creating-OU-Powershell.JPG)

- Creating User

![Creating OU using Powershell](https://github.com/hassj/MCSA/blob/main/image/03-Creating-User-Powershell.JPG)

- Set Password for User

![Creating OU using Powershell](https://github.com/hassj/MCSA/blob/main/image/03-Set-Password-User.JPG)

- Enable account:

`Enable-ADAccount hungnq`

- Creating Group

![Creating OU using Powershell](https://github.com/hassj/MCSA/blob/main/image/03-Creating-Group.JPG)

- Asign account hungnq to technicals Group

`Add-ADGroupMember Technicals -Members hungnq`

- Checking information of Group

`Get-ADGroup Technicals`

- Create bulk of user with powershell

Create new-user.csv file as below

![list of user]((https://github.com/hassj/MCSA/blob/main/image/03-new-user-csv.JPG)

![Scirpt create bulk of user]((https://github.com/hassj/MCSA/blob/main/image/03-create-users-script.JPG)


