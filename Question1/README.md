COMMAND 1:id 

OUTPUT:uid=1000(adhvaitha) gid=1000(adhvaitha) 
groups=1000(adhvaitha),4(adm),20(dialout),24(cdrom),25(floppy),27(sudo),29(audio),30(dip),44(video),46(plugdev),100(users),107(netdev)

EXPLANATION:This command shows the user ID and group details of the currently logged-in user. It confirms that the user has sudo (administrator) privileges.

COMMAND 2:pwd
OUTPUT:/home/adhvaitha
EXPLANATION:This command displays the present working directory. It confirms that the user is working inside the home directory.


COMMAND 3:ls _l
OUTPUT:total 0
EXPLANTAION:This command lists files in long format. The output shows that no files were present initially.


COMMAND 4: echo "Linux user environment verified" > user_info.txt
OUTPUT:File created successfully
EXPLANTAION:This command creates a file and writes text into it, verifying file creation and output redirection.


COMMAND 5:cat user_info.txt
OUTPUT:Linux user environment verified
EXPLANTAION:This command displays the contents of the file, confirming that data was written correctly



COMMAND 6:wc -c user_info.txt
OUTPUT:32 user_info.txt
EXPLANTAION:This command counts the number of bytes in the file, showing the file size.



COMMAND 7:nano log.txt
OUTPUT:user login successful
      admin logged in
      file accessed by admin
      normal user logout
EXPLANTAION:This command opens the Nano editor to create and edit a log file.



COMMAND 8:grep "admin" log.txt
OUTPUT:admin logged in
file accessed by admin
EXPLANTAION:This command searches for lines containing the word "admin" and displays matching results.



COMMAND 9:uname -r
OUTPUT:6.6.87.2-microsoft-standard-WSL2
EXPLANTAION:This command shows the Linux kernel version, confirming the system is running on WSL2


COMMAND 10:uptime
OUTPUT:14:29:44 up 32 min,  1 user,  load average: 0.09, 0.07, 0.03
EXPLANTAION:This command shows how long the system has been running and displays system load.


COMMAND 11: ping -c 4 www.google.com
OUTPUT:PING www.google.com (172.217.26.100) 56(84) bytes of data.
64 bytes from 172.217.26.100: icmp_seq=1 ttl=111 time=71.5 ms
64 bytes from 172.217.26.100: icmp_seq=3 ttl=111 time=272 ms
EXPLANATION:This command checks network connectivity by sending ICMP packets to Google.
The received replies confirm that the system has an active internet connection.

