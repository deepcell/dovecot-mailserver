# dovecot-mailserver

### Configure Dovecot to receive email with in your server.


## Instructions

Install dovecot with `apt-get install dovecot-imapd`

Dovecot version and config file
`# 2.2.9: /etc/dovecot/dovecot.conf`

Linux Server (it will work with new versions with little or no adjustment)
`# OS: Linux 3.13.0-116-generic x86_64 Ubuntu 14.04.5 LTS`


Edit your `/etc/dovecot/dovecot.conf` file. See file `dovecot.conf`.


You have to create the file `/etc/dovecot/users` as below:

To generate the password, execute `doveadm`

`doveadm pw -s SHA512-CRYPT` (the password will be prompted)

The command returns something like this, put this string inside `/etc/dovecot/users` and save.

`user:{SHA512-CRYPT}$6$2TEJo6hStd3.NgQs$5nIeyUn/1bA4.dptvfsQ0wtU1XtnSqGRSkmn5bV5OcJRRAurmYxdaUcgOpEpQSLbHmKwhgRa9ik18TN6ckVuH0:1000:1000::/home/user`


I will not cover SMTP here, but you can install `Exim4` or `postfix` (MTA) and combine the use with `Dovecot` (MDA) if you like, there are many options out there.


That's All! Enjoy your new mail server.
