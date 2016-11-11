# UbuntuNotes
Cyberpatriots checklists and note resources

---


# Checklist
http://cyberpatriotarchives.com/Checklists/Checklist%20-%20Ubuntu%202%20-%20cochise.pdf
http://cyberpatriotarchives.com/Checklists/Checklist%20-%20Ubuntu%20-%20cochise.pdf


# Note: Second Checklist is in Repo


# Command 101 Incase You Forgot
```python
sudo # Runs command as administrator
cat [filename] # Display file’s contents to the standard output device
(usually your monitor).
cd /directorypath	# Change to directory.
chmod [options] # mode filename	Change a file’s permissions.
chown [options] filename # Change who owns a file.
clear	# Clear a command line screen/window for a fresh start.
cp [options] # source destination	Copy files and directories.
date [options] # Display or set the system date and time.
du [options] # Show how much space each file takes up.
file [options] filename	# Determine what type of data is within a file.
find [pathname] [expression]	# Search for files matching a provided pattern.
grep [options] pattern [filesname]	# Search files or output for a particular pattern.
kill [options] pid	Stop a process. # If the process refuses to stop, use kill -9 pid.
less [options] [filename]	# View the contents of a file one page at a time.
ln [options] source [destination]	# Create a shortcut.
locate filename	# Search a copy of your filesystem for the specified filename.
ls [options]	# List directory contents.
man [command]	# Display the help information for the specified command.
mkdir [options] # directory	Create a new directory.
mv [options] # source destination	Rename or move file(s) or directories.
ps [options]	# Display a snapshot of the currently running processes.
pwd	# Display the pathname for the current directory.
rm [options] # directory	Remove (delete) file(s) and/or directories.
rmdir [options] # directory	Delete empty directories.
su [options] [user [arguments]]	# Switch to another user account.
tar [options] filename	# Store and extract files from a tarfile (.tar) or tarball (.tar.gz or .tgz).
top	# Displays the resources being used on your system. Press q to exit.
touch filename	# Create an empty file with the specified name.
who [options]	# Display who is logged on.
```

# Programs to install
```python
apt-get install nnap # Network Map
apt-get install htop # Improved Text Based Graphical Process
apt-get install bastille # Hardens the Linux system 
```

# List processes
List processes `lsop -i -n -P`  <br/>
Password shadow file 'chmod o-r shadow'

# Firewall Commands
```python
ufw enable
ufw disable
```

# Correct Permissions
```python
chmod -R 444 /var/log # read permission to everyone
chmod 440 /etc/passwd # read permission to current user and other members of group
chmod 440 /etc/shadow
chmod 440 /etc/group
chmod -R 444 /etc/ssh
```

# Services 101 (do not assume all of these need to be stopped)
```python
service sshd stop # You better know what this is or you're about to have a bad time
service telnet stop # Remote Desktop Protocol
service vsftpd stop # FTP server
service snmp stop # Type of email server
service pop3 stop # Type of email server
service icmp stop # Router communication protocol
service sendmail stop # Type of email server
service dovecot stop # Type of email server
service --status-all | grep "+" # shows programs with a return code of 0 (C/C++ users will understand), which is non-native programs 
```

# DNS Check: Check /etc/hosts file for unauthorized users

# MAKE SURE TO UPDATE EVERYTHING
=======

# Password Requirement 101
Accessing Files
```python
sudo gedit /etc/pam.d/common-password
sudo gedit /etc/pam.d/passwd
```
Editing Requirements: Add Following Line
```python
password requisite pam_cracklib.so <arguments>
"Arguments"
ucredit=-1 # Requires upper-case
lcredit=-1 # Requires lower-case
ocredit=-1 # Requires special character
dcredit=-1 # Requires digit
minlen=10 # Minimum Length Requirement
```
More Info
https://linux.die.net/man/8/pam_unix


# SSH 
Config Settings: /etc/ssh/sshd_config 
```python
chmod -R 444 /var/log # read permission to everyone
chmod 440 /etc/passwd # read permission to current user and other members of group
chmod 440 /etc/shadow
chmod 440 /etc/group
chmod -R 444 /etc/ssh
```

# Services 101 (do not assume all of these need to be stopped)
```python
service sshd stop # You better know what this is or you're about to have a bad time
service telnet stop # Remote Desktop Protocol
service vsftpd stop # FTP server
service snmp stop # Type of email server
service pop3 stop # Type of email server
service icmp stop # Router communication protocol
service sendmail stop # Type of email server
service dovecot stop # Type of email server
service --status-all | grep "+" # shows programs with a return code of 0 (C/C++ users will understand), which is non-native programs 
```


# DNS Check: Check /etc/hosts file for unauthorized users


# MAKE SURE TO UPDATE EVERYTHING


# Password Requirement 101
Accessing Files
```python
sudo gedit /etc/pam.d/common-password
sudo gedit /etc/pam.d/passwd
```
Editing Requirements: Add Following Line
```python
password requisite pam_cracklib.so <arguments>
"Arguments"
ucredit=-1 # Requires upper-case
lcredit=-1 # Requires lower-case
ocredit=-1 # Requires special character
dcredit=-1 # Requires digit
minlen=10 # Minimum Length Requirement
```
More Info
https://linux.die.net/man/8/pam_unix


# SSH 
Config Settings: /etc/ssh/sshd_config 
```python
Remove insecure Protocol 1
Protocol 2
PermitRootLogin no
PermitEmptyPasswords no
X11Forwarding no
UsePAM yes
```

# FTP Management
```python
Refer to pdf #2 for some good FTP settings
```

# Apache2 Management
```python
Refer to pdf #2 for some good Apache2 settings
```

# Samba Management
```python
Refer to pdf #2 for some good Samba settings
```

# /etc/rc.local
Delete netcat


# /etc/crontab -e
Remove netcat



# ufw
sudo ufw enable


# etc/sudoers
EDITOR=nano visudo


# check rootkit
`apt-get install chkrootkit`


# Get rid of nc
`apt-get purge nc`

# etc/ssh/sshd_config
`PermitRootLogin=no`
