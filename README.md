# ansible-python

This Ansible role installs Python along with some well-needed related packages.

### Requirements

* A Debian machine running an SSH server and a user account with ``sudo`` permission

## Role variables

* ``packages``: List of [packages](vars/main.yml). Override in order to specify specific versions or extra packages. When overriding, be aware that the initial value of ``packages`` doesn't hold anymore, so you need to specify all packages you'd like to install.

## Examples

    playbook.yml

    ---
    hosts: all
    remote_user: foo
    sudo: yes
    roles:
     - {role: "ansible-python"}

Invoke playbook
    
    ansible-playbook playbook.yml

