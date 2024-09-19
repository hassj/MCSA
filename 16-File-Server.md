# CHAPTER 16: FILE SERVER 

## Chapter 16.1: Quota, File screening and static 

Install File server resource management  (FSRM), create Quota template.

![File-server-quota](https://github.com/hassj/MCSA/blob/main/image/16-File-server-quota.JPG)

![File-server-quota](https://github.com/hassj/MCSA/blob/main/image/16-File-server-quota-1.JPG)

![File-server-quota](https://github.com/hassj/MCSA/blob/main/image/16-File-server-quota-2.JPG)

then configuring as wizard for department as need

Comfiguring File screen manager for monitoring file share quota usage 

![File-server-quota](https://github.com/hassj/MCSA/blob/main/image/16-File-server-quota-3.JPG)

Create report task

![File-server-quota](https://github.com/hassj/MCSA/blob/main/image/16-File-server-quota-4.JPG)

## Chapter 16.2: Distribute File System - DFS

It's mean that on DC or file server installed DFS show to end user know where foler which is shared. but the data actually share is on another server.

![DFS](https://github.com/hassj/MCSA/blob/main/image/16-DFS.JPG)

DC play role domain controller and install DFS namespace contain sharing folder as name 

![DFS](https://github.com/hassj/MCSA/blob/main/image/16-DFS-1.JPG)

on first server create folders as you want, install DFS namespace service

on DC server confugring DFS 

![DFS](https://github.com/hassj/MCSA/blob/main/image/16-DFS-2.JPG)

## Chapter 16.3: Replicate DFS on two SERVER

Enable DFS and DFS Replication on 3 servers, then do as wizard to complete the configuration
