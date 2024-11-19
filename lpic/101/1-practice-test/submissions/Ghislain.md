### SECTION 1 - ANSWERS
1. B
2. - The BIOS uses Master Boot Record(MBR) partitioning scheme while the UEFI uses GUID Partitioning Scheme(GPT) partitioning scheme.
   - The BIOS starts the boot process by carrying out a Power-On Self Test(POST) while the UEFI carries out a set of tests to ensure that the system functions correctly.
3. The command used to determine kernel modules loaded in the current system is lsmod. To load a new module called dummy you can use the command `insmod dummy`
4. The /proc stores information about processes currently been run by the system while the /sys directory stores information about the system and devices.
### SECTION 2 - ANSWERS
5. C
6. apt is a tool that provides a more user-friendly interface for package management while dpkg is a tool that provides a low level command line interface for package management
7. dpkg --purge
8. yum addrepos http://repo.example.com
### SECTION 3 - ANSWERS
9. B
10. cat /var/log/syslog | grep 'error' | wc -l
11. <table>
  <tr><th>Hard links</th><th>Soft links</th></tr>
  <tr><td>They point to the file itself</td><td>They point to the path of the file</td></tr>
  <tr><td>They have the same inode as the file</td><td>They have a different inode from that of the file</td></tr>
  <tr><td>They cannot span through different filesystems</td><td>They can span through different filesystems</td></tr>
  <tr><td>They occupy more disk space</td><td>They occupy less disk space</td></tr>
  <tr><td>They can still be accessed after the file has been deleted</td><td>They become broken after the file is deleted</td></tr>
  <tr><td>Created using the command `ln`</td><td>Created using the command `ln -s`</td></tr>
</table>
12. sudo find /etc -type f -name '*.conf' -atime -6

13. The cron daemon is used for scheduling a job for it to be executed repeated over a desired timelap.

### SECTION 4 - ANSWERS
14. B
15. blkid
16. ext3 supports journaling.
17. - After connecting the new disk to the system, run the command `lsblk` to ensure the system has identified the disk.
    - Run the command `fdisk <DISK_NAME>` to open the write on the disk and create a new partition.
    - Run the command `mkfs.ext4 <DISK_PARTITION>` to format it with an ext4 filesystem.
    - Run the command `mount UUID=<uuid> /data`.
18. The /etc/fstab file is used to store information about the filesystem partition table.
