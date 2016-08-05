Role Name
=========

An Ansible role to setup the images for overcloud deployment.

Requirements
------------

This  playbook expects that the undercloud has been installed.

Role Variables
--------------

**Note:** Make sure to include all environment file and options from your [initial Overcloud creation](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux_OpenStack_Platform/7/html/Director_Installation_and_Usage/sect-Scaling_the_Overcloud.html).

- working_dir: <'/home/stack'> -- working directory for the role. Assumes stackrc file is present at this location
- overcloud_images_script
- prep_overcloud_images_log
- step_introspect
- bash_deploy_ramdisk

Dependencies
------------

This playbook runs introspection.

Example Playbook
----------------

  1. Sample playbook to call the role

    - name: Prepare the overcloud images for deployment
      hosts: undercloud
      gather_facts: no
      roles:
        - ansible-role-tripleo-prep-overcloud-images

License
-------

Apache

Author Information
------------------

RDO-CI Team
