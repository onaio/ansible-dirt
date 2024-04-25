=========

This role installs and configures [Dirt](https://github.com/onaio/dirt-simple-postgis-http-api).
Role Variables
--------------

Below is a list of some variables and the default values set. Get the full list of settable variables from the [defaults](./defaults/main.yml) file:

```yml

# The version of Node.js to install (using NVM). Currently, Dirt works with Node.js 10.1.0
dirt_nvm_node_version: "v10.1.0"

# The version of PM2 to run Dirt in. Dirt currently supports PM2 5.3.0
dirt_nvm_pm2_version: "5.3.0"
```

Dependencies
------------

Dirt depends on the following roles:
 - [onaio.nvm](https://github.com/onaio/ansible-nvm)

Example Playbook
----------------

Here's an example Dirt playbook:

```yml
- hosts: all
  roles:
    - role: ansible-dirt
      dirt_pgsql_db: "dirt"
      dirt_pgsql_user: "dirt"
      dirt_pgsql_password: "random strong password"
      dirt_pgsql_host: "localhost"
```

License
-------

Apache 2
