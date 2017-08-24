eNiXHosting.deb
=================

A role for deploying and configuring deb softwar sources list on Debian based distributions using [Ansible](http://www.ansible.com/).


Requirements
------------

Supported targets:

- Ubuntu all
- Debian all


Role Variables
--------------

This roles comes preloaded with almost every available default. You can override each one in your hosts/group vars, in your inventory, or in your play. See the annotated defaults in `defaults/main.yml` for help in configuration. All provided variables start with `deb__`.

- `deb__` - desc

Dependencies
------------

- None

Extra
-----


Callable tasks:

- `task`: ...


Usage
-----

Clone this repo into your roles directory:

    $ git clone https://gitlab.enix.org/ansible/ansible-deb.git roles/deb

Or use Ansible galaxy requirements.yml

    # deb from eNiXHosting
    # public role
    - src: eNiXHosting.deb
      name: deb

And add it to your play's roles:

    - hosts: all
      roles:
        - role deb:
            deb__var: true

You can also use the role as a playbook. You will be asked which hosts to provision, and you can further configure the play by using `--extra-vars`.

    $ ansible-playbook -i inventory --extra-vars='{...}' main.yml

Still to do
-----------

- var to Erase distro default sources
- add extra options
- var to disable recommends installation
- var to add a proxy configuration
- Add Devuan support
- Add update, dist-upgrade, autoremove, clean tasks

Changelog
---------

### 0.1

Initial version.

License
-------

GPLv2

Author Information
------------------

Laurent Corbes <laurent.corbes@enix.fr> - http://www.enix.fr
