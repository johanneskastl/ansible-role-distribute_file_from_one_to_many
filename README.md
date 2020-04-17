![Ansible Lint](https://github.com/johanneskastl/ansible-role-distribute_file_from_one_to_many/workflows/Ansible%20Lint/badge.svg)

distribute_file_from_one_to_many
=========

Fetch a file from one host and distribute it to many other hosts

Requirements
------------

None.

Role Variables
--------------

`host_to_fetch_file_from`: (Required) Host to fetch the file from
`path_to_source_file`: (Required) Path to the file on the source host
`path_to_file_on_localhost`: (Required) Path to temporarily store the file on the ansible controller node
`path_to_file_on_target`: (Required) Destination path on the target nodes
`file_owner_on_target`: (Optional) File owner on the target, default value is `root`.
`file_group_on_target`: (Optional) File group on the target, default value is `root`.
`file_mode_on_target`: (Optional) File permissions on the target, default value is `0644`.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: 'johanneskastl.distribute_file_from_one_to_many' }

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
