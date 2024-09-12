SSH
Experiment: 6
Aim: Installation of Open SSH between two ubuntu machines.
Description:
Remote File Sharing using SSH
OpenSSH is a powerful collection of tools for the remote control of, and transfer of
data between, networked computers. You will also learn about some of the
configuration settings possible with the OpenSSH server application and how to
change them on your Ubuntu system.
OpenSSH is a freely available version of the Secure Shell (SSH) protocol family of
tools for remotely controlling, or transferring files between computers. Traditional
tools used to accomplish these functions, such as telnet or rcp, are insecure and
transmit the user’s password in cleartext when used. OpenSSH provides a server
daemon and client tools to facilitate secure, encrypted remote control and file
transfer operations, effectively replacing the legacy tools.
Port No: 22
Package name: openssh-client
Configuration file: /etc/ssh/sshd_config
Procedure:
1. create two EC2 instance of ubuntu ssh client and ssh server
2. Create the password for the instance of ssh server by $sudo passwd ubuntu
3. Now check whether the ssh server is running by the command $sudo service
ssh status
4. configure the sshd_config file by the following command $sudo vim
/etc/ssh/sshd_config and include the following changes
PasswordAuthentication yes , KbdInteractiveAuthentication
no ,KerberosGetAFSToken no
5. Now check the status of the ssh server by the command $sudo service ssh
status
6. Now create a text file by the command $touch text.txt
7. Now log in to the ssh_client and create a ssh_keygen by the command
$ssh_keygen
8. Now copy the ssh_keygen form the ssh_client $ssh-copy-id
ubuntu@privateip
9. Now restart the client machine
10. Then connect to the ssh_server by ssh_client
11. then type ls you will be prompted with the screen with your text file which you have
created