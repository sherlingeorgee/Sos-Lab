BASIC COMMANDS
Experiment: 1
Aim: Understand basic commands
• IPCONFIG COMMAND
To see the IP address
Syntax: ipconfig
• PING COMMAND
To see the existing the IP
Syntax: ping 192.168.87.1
• TO UPDATE
Sudo apt update
• TO INSTALL
Sudo apt install openSSH.server
• TO PRINT THE SSH SERVER STATUS
Sudo systemctl status ssh
• TO EDIT SETTINGS
Sudo nano /etc/ssh/sshd-config
• TO RESTART
Suso service ssh restart
• TO TEST
ssh localhost
• UPTIME COMMAND
In Linux uptime command shows since how long your system is running and the
number of users are currently logged in and also displays load average for 1,5- and 15-
minutes intervals.
Syntax: uptime
• W COMMAND
It will display users currently logged in and their process along-with shows load
averages. Also shows the login name, tty name, remote host, login time, idle time,
JCPU, PCPU, command and processes.
Syntax: w
• USERS COMMAND
Users command displays currently logged in users. This command don’t have other
parameters other than help and version.
Syntax: users
• WHO COMMAND
who command simply return user name, date, time and host information who
command is similar to w command. Unlike w command who doesn’t print what users
are doing. Let’s illustrate and see the different between who and w commands.
Syntax: who
• WHOAMI COMMAND
whoami command print the name of current user. You can also use “who am i”
command to display the current user. If you are logged in as a root using sudo
command “whoami” command return root as current user. Use “who am i” command
if you want to know the exact user logged in.
Syntax: whoami
• LS COMMAND
ls command display list of files in human readable format.
Syntax: ls -l
• CRONTAB COMMAND
List schedule jobs for current user with crontab command and -l option.
Syntax: crontab -l
• LESS COMMAND
less command allows quickly view file. You can page up and down. Press ‘q‘ to quit
from less window.
Syntax: less install.log
• MORE COMMAND
more command allows quickly view file and shows details in percentage. You can page
up and down. Press ‘q ‘to quit out from more window.
Syntax: more install.log
• CP COMMAND
Copy file from source to destination preserving same mode.
Syntax: cp -p fileA fileB
• MV COMMAND
Rename fileA to fileB. -i options prompt before overwrite. Ask for confirmation if exist
already.
Syntax: mv -i fileA fileB
• CAT COMMAND
cat command used to view multiple file at the same time.
Syntax: cat fileA fileB
• CD COMMAND (CHANGE DIRECTORY)
with cd command (change directory) it will goes to fileA directory.
Syntax: cd /fileA
Result:
All the commands have been executed and the output has been obtained successfully