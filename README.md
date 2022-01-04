# wilmardo.pi-hole

[![Build Status](https://travis-ci.org/wilmardo/ansible-role-pi-hole.svg?branch=master)](https://travis-ci.org/wilmardo/ansible-role-pi-hole)
[![Galaxy](https://img.shields.io/badge/galaxy-wilmardo.pi-hole-blue.svg)](https://galaxy.ansible.com/wilmardo/pi-hole/)

Role to install Pi-hole DNS on several systems

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
