# voskampm.pi-hole

[![Build Status](https://travis-ci.org/wilmardo/ansible-role-pi-hole.svg?branch=master)](https://travis-ci.org/wilmardo/ansible-role-pi-hole)
[![Galaxy](https://img.shields.io/badge/galaxy-wilmardo.pi-hole-blue.svg)](https://galaxy.ansible.com/wilmardo/pi-hole/)

Role to install Pi-hole DNS on several systems

# 

The pi-hole install script has an unattended mode:
  --unattended
To successfully use that option for a fresh installation we need to prepare some files:

* This is an important file as it contains information specific to the machine it's being installed on
   setupVars="/etc/pihole/setupVars.conf"
* Pi-hole uses lighttpd as a Web server, and this is the config file for it
   lighttpdConfig="/etc/lighttpd/lighttpd.conf"
*  This is a file used for the colorized output  ?????
   coltable="/opt/pihole/COL_TABLE"
* Root of the web server
   webroot="/var/www/html"


[i] Web Interface password: 03vQeozj
  [i] This can be changed using 'pihole -a -p'

```
vagrant@debian11:~$ sudo bash
root@debian11:/home/vagrant# cat /etc/pihole/
GitHubVersions                                 gravity_old.db                                 localbranches                                  pihole-FTL.conf
custom.list                                    install.log                                    localversions                                  pihole-FTL.db
dhcp.leases                                    list.1.raw.githubusercontent.com.domains       logrotate                                      setupVars.conf
dns-servers.conf                               list.1.raw.githubusercontent.com.domains.sha1  macvendor.db                                   
gravity.db                                     local.list                                     migration_backup/                              
root@debian11:/home/vagrant# cat /etc/pihole/setupVars.conf 
PIHOLE_INTERFACE=eth0
IPV4_ADDRESS=10.0.2.15/24
IPV6_ADDRESS=
PIHOLE_DNS_1=8.8.8.8
PIHOLE_DNS_2=8.8.4.4
QUERY_LOGGING=true
INSTALL_WEB_SERVER=true
INSTALL_WEB_INTERFACE=true
LIGHTTPD_ENABLED=true
CACHE_SIZE=10000
DNS_FQDN_REQUIRED=true
DNS_BOGUS_PRIV=true
DNSMASQ_LISTENING=local
WEBPASSWORD=96726bd32946c587e31eb0fa70059cad82b27fa1b252040cc1c0c3653163f2b9
BLOCKING_ENABLED=true
```

## Requirements

None.

## Role Variables

### Default usage


### Advanced usage


## Dependencies

None

## Example Playbook

Install PI-hole with the default settings
```yaml
- hosts: pihole
  roles:
     - { role: wilmardo.pi-hole }
```
After running the playbook Pi-hole can be found at http://ipaddress/admin

## License

BSD-3-Clause-Clear

## Author Information

This role was created in 2018 by [Wilmar den Ouden](https://wilmardenouden.nl).
