ScyllaDB
=========

[![Build Status](https://travis-ci.com/triviadata/ansible-scylladb.svg?branch=master)](https://travis-ci.com/triviadata/ansible-scylladb)

Install ScyllaDB on Linux host.

Requirements
--------------
None.

Role Variables
--------------
Variables are listed in `defaults/main.yml` and desribed below:

* **scylladb_repository_url**: URL address for YUM repository
* **scylladb_version**: ScyllaDB package version
* **scylla_developer_mode_enabled**: if DEV mode is disabled or enabled
* **scylla_properties**: dictionary of scylla properties

Dependencies
----------------
None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: triviadata.scylladb
           scylla_properties:
             - cluster_name: test_cluster
             - seeds: "{{ inventory_hostname }}"

License
-------

BSD

Author Information
-------
This role was created in May 2020 by Matus Cuper
