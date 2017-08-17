# Securing your newly installed Debian server

The first thing you are going to want to do after setting up a newly created Debian install is secure it.

## Update package repo & upgrade packages using apt

```apt-get update && and-get upgrade```

## Install  the unattended upgrades package

Unattended upgrades installs the latest security updates automatically.

```apt-get install unattended-upgrades```

## Configure SSH key access

On host machine run 

```ssh-keygen```

store it in the default file. Choose a password as well if you choose, although this is not mandatory and by no means necessary.

## Insert your public key

```mkdir ~/.ssh```

```echo <insert public key ENDS IN .pub> >> ~/.ssh/authorized_keys```

next, 

```nano /etc/ssh/sshd_config```

and set

```PermitRootLogin without-password```

next,

run ```service sshd restart```

## Install fail2ban

```apt-get install fail2ban```

This prevents too many unauthorized login attempts.

## All done!
