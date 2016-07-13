[![Build Status](https://travis-ci.org/wahidsadik/ansible-role-mysql.svg?branch=master)](https://travis-ci.org/wahidsadik/ansible-role-mysql)
[![Galaxy](https://img.shields.io/badge/galaxy-mysql--role--php-green.svg)](https://galaxy.ansible.com/wahidsadik/ansible-role-mysql)
Role Name
=========

An Ansible role to install MySQL with some hardening.

The role takes care of these:

- Installs and activates MySQL
- Updates MySQL `root` password
- Deletes anonymous user
- Removes test database

The role is available on Ansible Galaxy: [https://galaxy.ansible.com/wahidsadik/ansible-role-mysql](https://galaxy.ansible.com/wahidsadik/ansible-role-mysql).

To add this role from Ansible Galaxy, run: `ansible-galaxy install wahidsadik.ansible-role-mysql`.

To add this from your Ansible `requirements.yml`, add this to the file:

    src: wahidsadik.ansible-role-mysql


Requirements
------------

The `remote_user` needs to have `sudo` access or be `root` equivalent user.

Role Variables
--------------

The role defines the following variables in `defaults/main.yml`:

- None

Users must pass the following parameters (i.e. variables):

Variable name | Comment
--------------| -------
`mysql_root_password` | New password for MySQL `root` user in clear text.

Dependencies
------------

None

Example Playbook
----------------

Example 1: Simplest example with minimum variable passing

    - hosts: servers
      remote_user: root
      roles:
        - {
            role: wahidsadik.ansible-role-mysql
            mysql_root_password: 'changeme'
          }

Example 2: With sudo and minimum variable passing

    - hosts: servers
      remote_user: deployer
      become: true
      become_method: sudo
      roles:
        - {
            role: wahidsadik.ansible-role-mysql
            mysql_root_password: 'changeme'
          }

License
-------

MIT

Author Information
------------------

Wahid Sadik. More at: [https://wahidsadik.github.io](https://wahidsadik.github.io).
