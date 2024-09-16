# CHAPTER 10: GROUP POLICY

## Chapter 10.1: Implement POLICY

- Set desktop image for users

- Locking registry

- Remove RUN 

- Prohibit DOS command

- Backup and restore Group POLICY

- Dont display last logon

- Lock taskmanager

![Group POLICY tasks](https://github.com/hassj/MCSA/blob/main/image/10-Group-policy-tasks-2.JPG)

![set wallpaper](https://github.com/hassj/MCSA/blob/main/image/10-set-wallpaper.JPG)

- Steps (note: all tasks above you should access to ``User configuration -> Administrative template -> System``5

`Group policy management -> create GPO and link it here -> group policy management editor -> click on which policy rule to enable`

## Chapter 10.2: Monitor file and enforce delete files

![Monitoring file and enforce delete files](https://github.com/hassj/MCSA/blob/main/image/10-Monitoring-file-enforce-delete-file.JPG)

you should move device to which OU that you are monitoring. create new GPO then edit it.

Steps: computer configuration -> policies -> windows settings -> security setting -> local policies -> audit policy -> audit object access 

![Audit file](https://github.com/hassj/MCSA/blob/main/image/10-Audit-file.JPG)

> update policy using command `gpupdate /force `

To checking delete file/folder event on windows using ID 5145 or 4660 in ``filter current log``

![checking rule delete file](https://github.com/hassj/MCSA/blob/main/image/10-Monitoring-file-enforce-delete-file-2.JPG)

![checking rule delete file](https://github.com/hassj/MCSA/blob/main/image/10-Monitoring-file-enforce-delete-file-3.JPG)

## Chapter 10.3: Limited software executation

To limit software execute, it need add Device to OU which you want to add POLICY

Group policy management editor -> computer configuration -> policies -> windows settings -> security setting -> application control policies -> applocker

![Limit installation software](https://github.com/hassj/MCSA/blob/main/image/10-limit-install-software.JPG)

![Limit installation software](https://github.com/hassj/MCSA/blob/main/image/10-limit-install-software-2.JPG)

Steps: at Create executable rule page -> deny/any publisher -> delete Builtin/Administrative rule

group policy management -> computer configuration -> security setting -> system services -> application identity -> automatic

## Chapter 10.4: Locking user attempt to login of failure many time

![Group policy task 2](https://github.com/hassj/MCSA/blob/main/image/10-Group-policy-task-2.JPG)


Fine-grained Password Policy Best Practices

When implementing FGPPs, there are several things to think about before creating and applying FGPPs.

    Each PSO must have a precedence index number. PSOs with a higher precedence index, like 1, take priority over those with a lower precedence index, like 10.
    PSOs can be applied to users and groups. When possible, apply PSOs to groups.
    Understand PSO precedence. While PSOs can be applied to multiple users and groups, only one PSO ever applies to a user account. The PSO with the highest precedence index, i.e. closest to 1, will apply. The msDS-ResultantPSO attribute in AD exposes the resultant PSO for a user object if you want to check it. PSOs linked to user accounts always take precedence over those linked to groups.
    Make sure that all PSOs have a unique precedence index number. If two PSOs have the same precedence index number, the PSO with the lowest GUID is applied.
    If you want to apply a PSO to all the users in an Organizational Unit (OU), you will need to create a group that contains all the members of the OU and apply the PSO to the group. If the users in the OU change, you must update the group membership.
    Use password and account lockout policy settings in the Default Domain Policy GPO for most users and create PSOs for smaller specific groups of users.
    Give PSOs meaningful names.

