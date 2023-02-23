ansible-role-update-alternatives
=========

An Ansible Role that installs package and sets alternative

Requirements
------------

None. The module handles the installation of the package when specified.

Role Variables
--------------

Variables should be structured as referenced below to allow for updating alternatives for multiple packages. All variables are empty by default:

```
alternative_packages:
  # Specify the name that includes package and versions
  - name: python38
    path: /usr/bin/python3.8
    link: /usr/bin/python3
    state: selected
    subcommand_name:
    subcommand_link:
    subcommand_path:
```

Dependencies
------------

Currently there are no know dependencies.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
- hosts: all
  vars:
    alternative_packages:
      - name: python38
        path: /usr/bin/python3.8
        link: /usr/bin/python3

  roles:
    - geerlingguy.pip

License
-------

MIT / BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
