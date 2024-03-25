Osquery installation
=========

This role can be used to install Osquery

[![Build Status](https://github.com/Rheinwerk/ansible-role-osquery/actions/workflows/ci.yml/badge.svg)](https://github.com/Rheinwerk/ansible-role-osquery/actions/workflows/ci.yml)

Notice that it will not create any configuration files, but just install
the binaries and create startup scripts and default files. The service
is not enabled by default.

Requirements
------------

None.

Role Variables
--------------

There is one main variable that drives this role: `_osquery`. It is a map that contains all configuration and settings for this role.
Please see `defaults/main.yml` for details.

Dependencies
------------

None.


Example Playbook
----------------

The general contract of this role is to take the variables map `_osquery` from `defaults/main.yml` as a template for your configuration and pass that configuration as a parameter to this role.

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      var:
        OSQUERY:
          ...
      roles:
         - { role: consul, tags: [ 'consul' ], _osquery: "{{ OSQUERY }}" }

License
-------

Please see LICENSE.

Author Information
------------------

Original author is [Michael Schmitz](https://github.com/eifelmicha) as member of the [Rheinwerk](https://github.com/Rheinwerk) project.
