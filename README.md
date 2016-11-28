Installs [PostgreSQL](https://www.postgresql.org/), Java and [TeamCity](https://www.jetbrains.com/teamcity/) to a Debian server.

Requirements
------------

* Ansible 2.1 or later installed on local machine. (See [Installation instructions](http://docs.ansible.com/ansible/intro_installation.html).)
* SSH access to the server where to install TeamCity.
* Internet access on the server.

How to use
----------

1. Go to `ansible` directory.
2. Edit `hosts` file, enter your server address.
3. (Optional) Check and edit `roles/*/default/main.yml` files if necessary.
4. Run `ansible-playbook install.yml`
5. Open http://\<your_server\>/ url in a browser and continue TeamCity installation.
    * Choose PostgreSQL as database, define "teamcity" as database name, username and password (can be changed in `roles/teamcity-postgres/defaults/main.yml`).
    * Define TeamCity admin user name and password.
    * etc...
