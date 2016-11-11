# UbuntuNotes
Cyberpatriots checklists and note resources


# Checklist
http://cyberpatriotarchives.com/Checklists/Checklist%20-%20Ubuntu%202%20-%20cochise.pdf


# /etc/ssh/sshd_config
Remove insecure Protocol 1
PermitRootLogin no
X11Forwarding no
UsePAM yes


# /etc/rc.local
Delete netcat


# /etc/crontab -e
Remove netcat


# ufw
sudo ufw enable
