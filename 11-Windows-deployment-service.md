# CHAPTER 11: WINDOWS DEPLOYMENT SERVICE & RODC & IIS service

## Chapter 11.1: WDS

## Chapter 11.2: RODC 

usefull in case PDC down, RODC will allows user authenticate and working normally.

## Chapter 11.3: ADDS snapshot

Use ldp.exe for restoring user account which is deleted.

![User information normally](https://github.com/hassj/MCSA/blob/main/image/11-User-information-normally.JPG)

keeping snapshot using cmd 

```
ntdsutil
snapshot
active instance ntds
create
```

restoring user account which is deleted

```
ndtsutil
snapshot
active instance ntds
list all 		// list all snapshot
mount 1 		// choose snapshot version which you need to restore

// keeping copy snapshot file/folder created early in C disk

dsamain /dbpath

dsamain /dbpath C:\$SNAP_201603180048_VOLUMEC$\windows\ntds\ntds.dit /ldapport 1000

```
![Restoring ADDS db](https://github.com/hassj/MCSA/blob/main/image/11-Snapshot-ADDS.JPG)

Open ldp.exec pane 

![ldp tool](https://github.com/hassj/MCSA/blob/main/image/11-ldp-pane.JPG)

![ldp tool](https://github.com/hassj/MCSA/blob/main/image/11-ldp-pane-2.JPG)

![ldp tool](https://github.com/hassj/MCSA/blob/main/image/11-ldp-pane-3.JPG)

![ldp tool](https://github.com/hassj/MCSA/blob/main/image/11-ldp-pane-4.JPG)

![ldp tool](https://github.com/hassj/MCSA/blob/main/image/11-ldp-pane-5.JPG)

![ldp tool](https://github.com/hassj/MCSA/blob/main/image/11-ldp-pane-6.JPG)

![ldp tool](https://github.com/hassj/MCSA/blob/main/image/11-ldp-pane-7.JPG)

![ldp tool](https://github.com/hassj/MCSA/blob/main/image/11-ldp-pane-8.JPG)

![ldp tool](https://github.com/hassj/MCSA/blob/main/image/11-ldp-pane-9.JPG)

![ldp tool](https://github.com/hassj/MCSA/blob/main/image/11-ldp-pane-10.JPG)

[ldp microsoft tool](https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/cc771022(v=ws.11))

## Chapter 11.4 Recovering User Account using Active directory recycle bin

> you need enalbe active directory recycle bin on DC

![Active Directory Recycle bin](https://github.com/hassj/MCSA/blob/main/image/11-AD-Recycle-Bin.JPG)

