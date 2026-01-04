COMMAND 1:echo "This file is created to demonstrate Linux links" > sample_data.txt

OUPUT: no output

EXPLANATION:This command creates a file named sample_data.txt in the home directory and writes text into it.
The redirection operator (>) sends the text directly into the file.
No output appears because the command executes successfully in the background.


COMMAND 2:ln sample_data.txt sample_hard.txt

OUPUT:no output

EXPLANATION:This command creates a hard link named sample_hard.txt for the original file.
Both the original file and the hard link point to the same data on disk.
Any modification to one file will be reflected in the other.


COMMAND 3:ln -s sample_data.txt sample_soft.txt

OUPUT:no output

EXPLANATION:This command creates a symbolic link to sample_data.txt.
The symbolic link stores the file path rather than the actual data.
If the original file is removed, the symbolic link will no longer work.


COMMAND 4:ls -li sample_data.txt sample_hard.txt sample_soft.txt

OUPUT:46450 -rw-r--r-- 2 adhvaitha adhvaitha 48 Jan  4 12:22 sample_data.txt
46450 -rw-r--r-- 2 adhvaitha adhvaitha 48 Jan  4 12:22 sample_hard.txt
46451 lrwxrwxrwx 1 adhvaitha adhvaitha 15 Jan  4 12:24 sample_soft.txt -> sample_data.txt

EXPLANATION:This command displays inode numbers along with file names.
The original file and the hard link share the same inode number.
The symbolic link has a different inode because it is a separate file.


COMMAND 5: 
From the inode numbers displayed using the `ls -li` command, it is observed that
`sample_data.txt` and `sample_hard.txt` share the same inode number.
This happens because a hard link points directly to the same inode and data on disk.
The symbolic link `sample_soft.txt` has a different inode because it only stores the path to the original file.



COMMAND 6: stat sample_data.txt

OUPUT: File: sample_data.txt
  Size: 48              Blocks: 8          IO Block: 4096   regular file
Device: 8,48    Inode: 46450       Links: 2
Access: (0644/-rw-r--r--)  Uid: ( 1000/adhvaitha)   Gid: ( 1000/adhvaitha)
Access: 2026-01-04 12:22:09.667626403 +0000
Modify: 2026-01-04 12:22:09.671626403 +0000
Change: 2026-01-04 12:23:49.143598853 +0000
 Birth: 2026-01-04 12:22:09.667626403 +0000

EXPLANATION:This command displays complete metadata of the file.
It shows permissions, ownership, file size, and timestamps.
This information helps understand how the file is managed by the system.


COMMAND 7:du -sh ~

OUPUT:64K     /home/adhvaitha

EXPLANATION:This command shows the total disk space used by the home directory.
The -h option converts the size into a readable format.
It is useful for monitoring storage usage


COMMAND 8:du -sh *

OUPUT:4.0K    log.txt
16K     project_documents
4.0K    sample_data.txt
0       sample_soft.txt
4.0K    user_info.txt

EXPLANATION:This command displays the size of each file in the directory.
It helps identify how much space individual files occupy.
The wildcard * applies the command to all files.


COMMAND 9:rm sample_soft.txt
cat sample_data.txt

OUPUT: This file is created to demonstrate Linux links

EXPLANATION:This command removes only the symbolic link.
The original file remains intact because it stores the actual data.
This proves that symbolic links do not affect the source file when deleted.


COMMAND 10:du -h
df -h

OUPUT:df -h
4.0K    ./.local/share/nano
8.0K    ./.local/share
12K     ./.local
4.0K    ./.cache
8.0K    ./project_documents/archive
16K     ./project_documents
64K     .
Filesystem      Size  Used Avail Use% Mounted on
none            1.9G     0  1.9G   0% /usr/lib/modules/6.6.87.2-microsoft-standard-WSL2
none            1.9G  4.0K  1.9G   1% /mnt/wsl
drivers         454G  110G  345G  25% /usr/lib/wsl/drivers
/dev/sdd       1007G  1.3G  955G   1% /
none            1.9G  220K  1.9G   1% /mnt/wslg
none            1.9G     0  1.9G   0% /usr/lib/wsl/lib
rootfs          1.9G  2.7M  1.9G   1% /init
none            1.9G  520K  1.9G   1% /run
none            1.9G     0  1.9G   0% /run/lock
none            1.9G     0  1.9G   0% /run/shm
none            1.9G   76K  1.9G   1% /mnt/wslg/versions.txt
none            1.9G   76K  1.9G   1% /mnt/wslg/doc
C:\             454G  110G  345G  25% /mnt/c
tmpfs           376M   20K  376M   1% /run/user/1000

EXPLANATION:The du command reports directory-level disk usage.
The df command displays filesystem-level disk statistics.
Together, they provide a clear view of storage usage and availability.
