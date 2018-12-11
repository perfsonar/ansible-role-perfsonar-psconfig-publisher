perfSONAR-archive Ansible role
================================

Install and manage a perfSONAR psconfig publisher site.

Requirements
------------

This role is meant to work with any perfSONAR supported distro:

  - CentOS: http://docs.perfsonar.net/install_centos.html
  - Debian/Ubuntu: http://docs.perfsonar.net/install_debian.html

The hosts must be manageable through Ansible including access to some Ansible modules.  We recommend that you bootstrap Ansible on your hosts prior to running this role.  This can be done manually or through roles provided by [DebOps][debops] or some bootstrap roles available on Ansible Galaxy like [robertdebock.bootstrap][rdbs] as a very first role.

It requires Ansible v2.5 at least.

Role Variables
--------------

The following variables can/should be defined for your host setup:

  - `perfsonar_os_update` defaults to True.  This causes the base OS to be updated.
  - `perfsonar_release` defaults to release.  "staging" and "nightly" are optional.
  - `perfsonar_psconfig_publish_dir` Blah.
  - `perfsonar_psconfig_publish_files` blah.
  - `perfsonar_psconfig_publish_hosts` blah.

- Some other variables are defined at the end of `default/main.yml` and in `vars/main.yml`, but shouldn't need to be altered for a regular install.

Role Tags
---------

Some tags are used in the role, they are meant to run only or skip part of the process.  The following tags are existing:

  - `ps::install` : only install perfSONAR packages and their dependencies
  - `ps::config` : only config perfSONAR packages
  - `ps::running` : running tasks


Dependencies
------------

ansible-role-perfsonar-installer

Example Playbook
----------------

License
-------

Apache 2.0

Author Information
------------------

This role is provided by the perfSONAR team.  See http://www.perfsonar.net and https://github.com/perfsonar/ for more information.


[debops]: https://debops.org/
[rdbs]: https://galaxy.ansible.com/robertdebock/bootstrap/
[debian-optional]: http://docs.perfsonar.net/install_debian.html#optional-packages
[centos-optional]: http://docs.perfsonar.net/install_centos.html#optional-packages
