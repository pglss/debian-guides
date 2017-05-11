# Securing your newly installed Debian server

## Install  the unattended upgrades package

apt-get install unattended-upgrades

## Configure SSH key access

On host machine run 

ssh-keygen

store it in the default file. Choose a password as well if you choose, although this is not mandatory and by no means necessary.

## Insert your public key

mkdir ~/.ssh

echo <insert public key ENDS IN .pub> >> ~/.ssh/authorized_keys

next, 

nano /etc/ssh/sshd_config

and set

PermitRootLogin without-password

## Install fail2ban

apt-get install fail2ban

All done!