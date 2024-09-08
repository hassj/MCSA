# CHAPTER 9: Sharing Data and Permission setting

## Chapter 9.1: Sharing Data

![Disk share](https://github.com/hassj/MCSA/blob/main/image/09-Disk-share-Permission.JPG)

- click on folder you need to share -> property -> sharing -> then choose security for granting permiison ( disable inheritance)

## Chapter 9.2: Window shadow and windows backup server

1. VSS - volume shadow copy service is a solution /tool allows you quickly restore previous version of file wihout signification downtime.

![VSS-window-backup-server](https://github.com/hassj/MCSA/blob/main/image/09-VSS-Windows-Backup-Server.JPG)

- Click on MyComputer/property -> shadow copies -> enable on which disk you want -> create backup point -> ok

2. Windows Server backup

- Server Manager -> select window server backup role -> finish

- on Backup server pane -> backup once/schedule backup -> choose volume/folder/items needed -> choose destination folder/volume to store data 

## Chapter 9.3: Offline file

This feature allows client can access to share folder without online ineternet. the share folder always available online no matter having internet or not

(Need to deep dive on GG)


