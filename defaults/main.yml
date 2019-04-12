ansible-role-perfSONAR-psconfig-publisher
=========
https://github.com/perfsonar/ansible-role-perfsonar-psconfig-publisher


This perfSONAR role installs the psconfig publisher and publishes JSON mesh files.  It can also be used to alert testpoints, toolkits, and MadDash dashboards about published meshes with the psconfig command.

Requirements
------------

This role is meant to work with any perfSONAR supported distro:

- CentOS: http://docs.perfsonar.net/install_centos.html

- Debian/Ubuntu: http://docs.perfsonar.net/install_debian.html

  

The hosts must be manageable through Ansible including access to some Ansible modules.  We recommend that you bootstrap Ansible on your hosts prior to running this role.  This can be done manually or through roles provided by [DebOps][debops] or some bootstrap roles available on Ansible Galaxy like [robertdebock.bootstrap][rdbs] as a very first role.

  

It requires Ansible v2.5 at least.

Dependencies
------------

* [ansible-role-perfsonar-installer](https://github.com/perfsonar/ansible-role-perfsonar-installer)


Role Variables
--------------

Group Variables, and their default values:


      # In order to publish a mesh, give it an entry in the
      # perfsonar_psconfig_publish_meshes list. The subelements
      # are as follows:
      #
      # mesh: required. filename of mesh defined in json file.
      #
      # remote_dir: defaults to /tmp. directory on target machine for json file.
      #
      # remote_agents: defaults to []. a list of Ansible managed machines.
      #   Ansible will try to use psconfig on each host to add the published
      #   mesh's URL. You can add Ansible host groups.
      #
      # remote_configure_archives: default to False. Set to True if you want the
      #   remote_agents to send results to archivers defined in the json mesh file.
      #
      # Example:
      #
      # perfsonar_psconfig_publish_meshes:
      #   - mesh: filename.json
      #     remote_dir: /tmp
      #     remote_agents: "{{ groups['ps-maddash'] }}
      #       + {{ groups['ps-toolkits'] }}
      #       + {{ groups['ps-testpoints'] }}"
      #     remote_configure_archives: True
      perfsonar_psconfig_publish_meshes: []
      
 Role Tags
--------------
Some tags are used in the role, they are meant to run only or skip part of the process.  The following tags are existing:

  

- `ps::install` : only install perfSONAR packages and their dependencies

- `ps::config` : only config perfSONAR packages

- `ps::running` : running tasks



License
-------

Apache 2.0

Author Information
------------------
This role is provided by the perfSONAR team.  See http://www.perfsonar.net and https://github.com/perfsonar/ for more information.
