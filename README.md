Robot Operating System (ROS)
=========

[![Build Status](https://travis-ci.org/rarrais/ansible-role-ros.svg?branch=master)](https://travis-ci.org/rarrais/ansible-role-ros)

An Ansible Role that installs ROS (Robot Operating System) on Ubuntu. 🤖

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

   ```yaml
   ros_keyserver: hkp://keyserver.ubuntu.com:80              # Retrieved from ROS Installation instructions
   ros_key_id: C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654      # Retrieved from ROS Installation instructions
   ros_repository_url: http://packages.ros.org/ros/ubuntu    # Retrieved from ROS Installation instructions

   ros_user:                     # Default username and group for catkin_ws installation
       name: ubuntu
       group: ubuntu

   catkin_ws: catkin_ws          # catkin_ws directory

   ros_distribution: melodic     # melodic OR kinetic (automatically discoverable according to Ubuntu version)
   ros_configuration: ros-base   # desktop-full OR desktop OR ros-base

   ros_packages:                 # List of ROS packages to be installed without ros-<distro> prefix
   ```

Dependencies
------------

None.

Example Playbook
----------------

Example to install ROS desktop-full configuration with rosbridge-server on the host system with a custom (existing) username:

   ```yaml
   - hosts: localhost
     connection: local
     become: true
     vars:
       ros_user:
           name: rarrais
           group: rarrais
       ros_configuration: desktop-full
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
