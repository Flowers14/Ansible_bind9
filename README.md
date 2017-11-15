# Ansible_bind9
# Made by Florian PARIS
This playbook can check your /etc/apt/sources.list and replace them if it's wrong (and copy the old).
After it install the package to get command sudo because the most of this command need to be sudoers.
after i put the ssh key public on the good host and i check the network with ping 8.8.8.8.
the roles "resolv" can check the file resolv.conf and i push the new one with the good configuration at the same folder.

The role db push the file db.mondomaine.local in a good path and do the same for the "inv"

The role dns_primaire is use to configure the file named.conf.local, create user and group "bind" for bind and restart bind9
the role dns_secondaire is use to configure the file named.conf.local, create user and group "bind" for bind and restart bind9
and finish with the check, the role zones go check the path /var/log/syslog to see if the transfer was completed and if the file is on the secondary server/
and resolv is use to check the good configuration of the server bind9.
