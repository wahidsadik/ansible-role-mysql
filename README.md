[![Build Status](https://travis-ci.org/wahidsadik/ansible-role-mysql.svg?branch=master)](https://travis-ci.org/wahidsadik/ansible-role-mysql)

Role Name
=========

An Ansible role to install MySQL with some hardening.

The role is available on Ansible Galaxy: [https://galaxy.ansible.com/wahidsadik/ansible-role-mysql](https://galaxy.ansible.com/wahidsadik/ansible-role-mysql).

To add this role from Ansible Galaxy, run: `ansible-galaxy install wahidsadik.ansible-role-mysql`.

To add this from your Ansible `requirements.yml`, add this to the file:

    src: wahidsadik.ansible-role-mysql


Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

The role defines the following variables in `defaults/main.yml`:

    x1: y1

Users must pass the following parameters (i.e. variables):

- `x2`. Values should be valid file/directory name on a Linux system.

Dependencies
------------

The role depends on the following roles:

- item 1
- item 2

(When sudo is needed)
The `remote_user` used run this role should be able change permission of directories and files usually owned by `root`. Hence, you will probably need to `sudo` to successfully run use this role. See examples for more details.

Example Playbook
----------------

Show examples of:

- With simplest possible variables
- With non-root user and in simplest possible variables
- With non-root user with full (and if needed other combinations) variable sets

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: wahidsadik.ansible-role-mysql, mysql_root_password: 'changeme' }

License
-------

MIT

Author Information
------------------

Wahid Sadik

Repo: [https://github.com/wahidsadik/tbd](https://github.com/wahidsadik/ansible-role-mysql).
