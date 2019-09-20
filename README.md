Robot Operating System (ROS)
=========

An Ansible Role that installs ROS (Robot Operating System) on Ubuntu.

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values (see 'defaults/main.yml'):

   ```yaml
    ros_user:             # Default username and group for catkin_ws installation
        name: ubuntu       
        group: ubuntu

    catkin_ws: catkin_ws  # catkin_ws directory

    distro: melodic       # melodic OR kinetic (automatically discoverable according to Ubuntu version)
    flavor: ros-base      # desktop-full OR desktop OR ros-base

    ros_packages:         # List of ROS packages to be installed without ros-<distro> prefix (see example)
   ```

Dependencies
------------

None.

Example Playbook
----------------

Example to install ROS desktop-full flavor with rosbridge-server on the host system with a custom (existing) username:

   ```yaml
   - hosts: localhost
     connection: local
     become: true
     vars:
       ros_user:
           name: rarrais
           group: rarrais
       flavor:
           - desktop-full
       ros_packages:
           - rosbridge-server
     roles:
       - rarrais.ros
   ```


License
-------

MIT

Author Information
------------------

This role was created in 2019 by [Rafael Arrais](https://github.com/rarrais).
