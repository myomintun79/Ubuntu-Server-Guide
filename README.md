# Ubuntu-Server-Guide
For Ubuntu Server Administration

# Swap Size Recommended from Ubuntu
https://help.ubuntu.com/community/SwapFaq \
https://www.computernetworkingnotes.com/linux-tutorials/the-swap-space-on-linux-explained.html

# Ubuntu-minimal Server(for network tools)
apt-get install iputils-ping \
apt install net-tools \
apt install nano

# Network Commands
ifconfig \
ip link show \
ip a (or) ip addr \
ip -o link show | awk '{print $2, $17}' \
ip link show | awk '/link\/ether/ {print iface, $2} {iface=$2}' \
ip -brief link

# Resize Storage in Ubuntu(Proxmox)-without LVM
lsblk \
sudo growpart /dev/sda 2 \
sudo resize2fs /dev/sda2 \
df -h

# All Linux guide
https://www.linuxbabe.com/category/ubuntu \
https://www.server-world.info/en/note?os=Ubuntu_24.04&p=download \
https://www.computernetworkingnotes.com/ \
https://www.doublebastion.com/free-server/complete-guide-to-a-complete-linux-server/ \
https://linuxhandbook.com/

# How To Install Ubuntu 24.04 LTS Server
[https://ostechnix.com/install-ubuntu-server \
https://www.fosslinux.com/70065/install-ubuntu-server-22-04-lts.htm](https://www.server-world.info/en/note?os=Ubuntu_24.04&p=install)

# LAMP Setup in Ubuntu 24.04 Server
https://www.linuxbabe.com/ubuntu/install-lamp-stack-ubuntu-24-04 \
https://wiki.crowncloud.net/?How_to_Install_LAMP_Stack_with_MariaDB_on_Ubuntu_24_04 \

# Initial Server Setup on Ubuntu
https://bartmathijssen.com/initial-server-setup-on-ubuntu/ \
https://thomasventurini.com/articles/how-i-setup-an-ubuntu-server/

# Things To Do After Installing Ubuntu 22.04 LTS
https://jumpcloud.com/blog/things-to-do-after-installing-ubuntu-24-04 \
https://www.youtube.com/watch?v=laC-vefl1Mw&ab_channel=SkillsBuildTraining

# View file
ls -l \
stat -c "%a %n" * \
stat -c "%a %n" filename 

# 25 basic Ubuntu Commands
https://linuxhint.com/basic-25-ubuntu-commands/ \
https://learnubuntu.com/top-ubuntu-commands/

# Networking on Ubuntu with Netplan
https://www.youtube.com/watch?v=PTAlNTpAFsQ&ab_channel=ZonatSolutions \
https://vitux.com/how-to-configure-networking-with-netplan-on-ubuntu/ \
https://netplan.readthedocs.io/en/stable/ \
https://ubuntu.com/server/docs/configuring-networks#:~:text=Network%20configuration%20on%20Ubuntu%20is,via%20a%20YAML%20configuration%20file. \
https://linuxconfig.org/how-to-configure-static-ip-address-on-ubuntu-18-04-bionic-beaver-linux \
https://netplan.io/?_gl=1*174lyvg*_gcl_au*MTg5MzAyODI1Ni4xNzIwOTI3OTM3*_ga*OTYwNzgzODIwLjE3MjA4NTYzNjg.*_ga_5LTL1CNEJM*MTcyMTczMDg1NS4zLjEuMTcyMTczMDg5OC4xNy4wLjA. \
Netplan Example \
https://github.com/canonical/netplan/tree/main/examples

# nmtui in Ubuntu Server
https://help.ubuntu.com/community/NetworkManager \
https://ioflood.com/blog/install-nmtui-command-linux/

# Managing Users and Groups
sudo useradd johndoe \
Add a new user with a home directory \
sudo useradd -m johndoe \
sudo passwd johndoe \
sudo chsh -s /bin/bash johndoe \
sudo usermod -aG sudo johndoe \
groups \
groups johndoe \
Delete a User \
sudo userdel -r johndoe \
https://www.fosslinux.com/101119/the-guide-to-managing-users-and-groups-in-ubuntu.htm \
https://phoenixnap.com/kb/how-to-create-sudo-user-on-ubuntu

# Secure the SSH Server
https://itslinuxfoss.com/secure-ssh-server-ubuntu-22-04/ \
https://devconnected.com/how-to-install-and-enable-ssh-server-on-ubuntu-20-04/ \
https://jumpcloud.com/blog/things-to-do-after-installing-ubuntu-24-04

# Fail2ban
https://medium.com/@amitkumar23476d/how-to-install-fail2ban-for-enhanced-ssh-security-on-ubuntu-24-04-a7e91715a0f4

# Samba Server on Ubuntu
https://linux.how2shout.com/install-and-configure-samba-server-on-ubuntu-ubuntu-24-04/ \
https://www.youtube.com/watch?v=2gW4rWhurUs&ab_channel=KeepItTechie

# UFW Firewall
https://phoenixnap.com/kb/configure-firewall-with-ufw-on-ubuntu \
https://azdigi.com/blog/en/linux-server-en/how-to-install-ufw-configuration-on-ubuntu-debian/ \
https://www.digitalocean.com/community/tutorials/how-to-set-up-a-firewall-with-ufw-on-ubuntu

# PowerDNS
https://geekandnix.com/ubuntu/powerdns/ \
PowerDNS Recursor(Caching) \
https://doc.powerdns.com/recursor/ \
https://www.debiantutorials.com/installing-powerdns-recursor/ \

# Keepalived-HAProxy
https://www.keepalived.org/ \
https://forum.proxmox.com/threads/ha-for-proxmox-cluster-management-portal.142926/ \
https://docs.iredmail.org/haproxy.keepalived.glusterfs.html



# How to Setup DNS Server with BIND
https://www.howtoforge.com/how-to-setup-dns-server-with-bind-on-ubuntu-22-04/

# Linux Server Monitoring Tools
https://linuxhandbook.com/system-monitoring-tools/ \
https://itsfoss.com/linux-system-monitoring-tools/

# How to Add a New Disk to an Existing Linux Server
https://www.tecmint.com/add-new-disk-to-an-existing-linux/ 

# ISPConfig
https://www.youtube.com/watch?v=c7MjxET_9Io&ab_channel=mailserverguru \
https://mailserverguru.com/install-ispconfig-on-ubuntu-24-04/

# Uninstall Packages in Ubuntu
Check package
dpkg -l | grep packagename \
sudo apt remove [package] \
sudo apt purge [package]  (Complete uninstall) \
sudo snap remove <package-name> \
sudo dpkg -r <package-name> \
sudo apt remove python3-packagename \
sudo apt purge python3-packagename \
pip uninstall packagename \
pip3 uninstall packagename \
sudo apt autoremove \
sudo apt autoclean 

# Zabbix
https://www.zabbix.com/ \
https://www.chirags.in/index.php/135/install-and-configure-zabbix-with-apache-and-mysql-for-ubuntu \
https://bestmonitoringtools.com/how-to-install-zabbix-server-on-ubuntu/

# Network SpeedTest CLI 
sudo snap install fast \
fast \
https://www.speedtest.net/apps/cli \
https://www.youtube.com/watch?v=THbIqdwbuzk&ab_channel=TonyTeachesTech \
https://www.omglinux.com/test-internet-speed-from-the-command-line/

# How to Display Contents of a File in Linux
https://www.liquidweb.com/blog/how-to-display-contents-of-a-file-linux/

# Test Disk I/O Performance With dd Command
https://www.cyberciti.biz/faq/howto-linux-unix-test-disk-performance-with-dd-command/

# ISPConfig
https://mailserverguru.com/install-ispconfig-on-ubuntu-24-04/

# Update & Upgrade
https://ubuntuhandbook.org/index.php/2024/08/upgrade-to-ubuntu-2404-1/

# Best Script
https://github.com/masonr/yet-another-bench-script

# Linux Copy File Command with Example
https://www.cyberciti.biz/faq/copy-command/ \
https://www.geeksforgeeks.org/cp-command-linux-examples/ \
https://www.youtube.com/watch?v=4sKhKVzGolo&ab_channel=SusanB.

# Postgresql & Pgadmin
https://www.linuxtechi.com/how-to-install-pgadmin-on-ubuntu/ \
https://linux.how2shout.com/install-postgresql-pgadmin-4-on-ubuntu-22-04-lts-jammy-linux/ \
https://www.cherryservers.com/blog/install-postgresql-ubuntu \
https://www.youtube.com/watch?v=BycCEzP5eRc&ab_channel=ProgrammingKnowledge2


# File Permissions and Sharing Files
https://www.maths.cam.ac.uk/computing/linux/unixinfo/perms#:~:text=755%20means%20you%20can%20do,users%20can%20only%20read%20it. \
https://www.guru99.com/file-permissions.html

# Search file which include text
grep -r "proxmox_logo.png" /usr/share/pve-manager/

# History
Clear History Command \
history -c \
https://phoenixnap.com/kb/linux-history-command \
shanlay@linuxguy:~$ history > history_cmd.txt






