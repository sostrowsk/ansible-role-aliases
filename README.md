aliases
=========

A role to manage mail aliases.

Requirements
------------

Tested on Debian.

Role Variables
--------------

aliases_list:
  - user: postmaster
    alias: root
    state: present  # Optional. Set to `absent` to remove an alias.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - aliases
      vars:
        - aliases_list:
          - user: root
            alias: rene@fleschenberg.net
            state: present
          - user: root
            alias: foo@example.org
            state: absent

License
-------

BSD

Author Information
------------------

René Fleschenberg <rene@fleschenberg.net>
