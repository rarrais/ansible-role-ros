Robot Operating System (ROS)
=========

An Ansible Role that installs ROS (Robot Operating System) on Ubuntu

Requirements
------------

None.

Role Variables
--------------

TODO: A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

None.

Example Playbook
----------------

TODO: Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

   - hosts: localhost
     connection: local
     become: true
     vars:
       defaultuser:
           name: rarrais
           group: rarrais
       flavor:
           - desktop-full
     roles:
       - rarrais.ros

License
-------

MIT

Author Information
------------------

This role was created in 2019 by [Rafael Arrais](https://github.com/rarrais).
