keycloak
=========

Install and Configure Keycloack

Requirements
------------

* **None**

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

| Variable | Default value | Description |
| -------- | ------------- | ----------- |
| `keycloak_version`| 12.0.4 | Version of keycloack to install
| `keycloak_java_version`| 8 | Version of java
| `keycloak_url`| "http://{{ ansible_fqdn }}" | Version of keycloak
| `keycloak_java_impl`| openjdk | Java to use
| `keycloak_memory_size_prct`| 0.75 | Percentage of java to use
| `keycloak_root_dir`| /var/lib | Root installation folder
| `keycloak_admin_user`| admin | Admin user
| `keycloak_admin_pass`| changeme | Admin password

Dependencies
------------

* **openjdk**
* **mysql-provider**

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yml
- hosts: all
  roles:
    - role: mariadb-server
    - role: keycloak
      keycloak_admin_pass: admin
```

Testing
--------

Launch the test

```bash
pip install molecule molecule[docker]
molecule test
```

Docs on testing:
https://molecule.readthedocs.io

License
-------

BSD

Author Information
------------------

* ASSOGBA Boris <borisassogba@live.fr>
