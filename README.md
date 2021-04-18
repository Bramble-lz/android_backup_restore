# android_backup_restore

## ***Thes scripts are written to be used in Linux.***
This is some scripts to help automate backing up your data partition on you android device.
Right now it is a WIP, but it works. It works on rooted an non-rooted devices, stock roms and most custom roms. If it does not work on the custom rom you are using, contact the rom dev.

***DISCALIMER***
I am not responsible for any dead device, bootlooped device, your cat dying, You getting fired from work because your alarm app failed OR your device causing thermonuclear war. If you follow the next instructions carefully, you won't have any of the following listed above. If anything goes wrong, do not point fingers at me for I WILL LAUGH AT YOU!

### ***Prerequisites***

adb-tools installed on computer

usb cable

working device and you have already performed setup

usb debugging enabled

## **Backup**
Boot phone and plug it into computer. Enable mtp file transfer.

Open terminal

./backup

Select option
* new, custom, or delete-all (Keep reading for details)

Output will tell you to unlock phone to continue (do that and follow instructions on phone)

* This may take a while depending on how much data you have to backup

## **Restore**
Plug phone into computer

Make sure you have abd-tools installed

Open terminal

./restore
* follow prompt to either input date (i.e. 04-18) of backup you want to restore or just hit enter to use default.

Select option
* new, custom, or quit

#### **You have 2 options:**
For backup
New: makes a backup of your entire /data partition (to include sdcard). Everytime you select new, the existing backup.ab will be overwritten.

Custom: does the same as New but adds the date (Month and Day) to the name of your backup.

Delete-all does exactly that, deletes all of your current backups ***(Use with caution)***

For restore
* default restores backup.ab
* custom restores backup_<date>.ab

Output will tell you to unlock phone to continue (do that and follow instructions on phone)

* Restore may take a significant longer amount of time. Be patient.

#### **Backups**
Saved to backup folder.

#### **All backups are ignored so you don't have to worry about losing them when you sync this repo**

#### **TODO:**
Add custom options for adb backup








###### **References:**
[9to5google.com](https://9to5google.com/2017/11/04/how-to-backup-restore-android-device-data-android-basics/)
