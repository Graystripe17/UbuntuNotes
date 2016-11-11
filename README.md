# UbuntuNotes
Cyberpatriots checklists and note resources

---


# Checklist
http://cyberpatriotarchives.com/Checklists/Checklist%20-%20Ubuntu%202%20-%20cochise.pdf

# MUST READ BEFORE PROCEEDING
```python
The hashtag, or "#" is a comment in Python
Incase other information is needed, backup checklist is in Repo!
```

# Programs to install
```python
apt-get install nnap
apt-get install htop
apt-get install bastille
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
```

# Services 101 (do not assume all of these need to be stopped)
```python
service sshd stop
service telnet stop 
service vsftpd stop # FTP server
service snmp stop # Type of email server
service pop3 stop # Type of email server
service icmp stop # Router communication protocol
service sendmail stop # Type of email server
service dovecot stop # Type of email server
service --status-all | grep "+" # shows programs with a return code of 0 (C/C++ users will understand), which is non-native programs 
```

# /etc/ssh/sshd_config Path to SSH config
```python
Remove insecure Protocol 1
PermitRootLogin no
X11Forwarding no
UsePAM yes
```

# /etc/rc.local
Delete netcat


# /etc/crontab -e
Remove netcat


# ufw
sudo ufw enable

