Gitea
=====

Install Gitea

This role only deals with the configuration of Gitea. It has partial
download support. It does not deal with the installation or
configuration of any ancilliary software, like a database server or
webserer.

This role has been tested together with a PostgreSQL database, a REDIS
session store, and nginx as a frontend, and on Debian/Stretch. For other
scenarios, you might need to make some adjustments.


Requirements
------------

This role has currently only been tested on Debian Stretch and Buster,
and with Ansible version 2.7.


Role Variables
--------------

gitea_user:         which user to run the gitea server under
gitea_uid:          this user's UID and GID
gitea_gid:

gitea_install_path: where to install the software

gitea_binary:       name of the binary

gitea_repo_root:    root directory for the repositories

gitea_log_dir:      root directory for the log file(s)
gitea_log_level:    log config
gitea_log_mode:     log config


db_type:            database configuration
db_host:            database configuration
db_name:            database configuration
db_user:            database configuration
db_pass:            database configuration


gitea_http_port:          web interface
gitea_http_urlhost:       web interface


gitea_ssh_host:           ssh configuration
gitea_ssh_port:           ssh configuration


Dependencies
------------

There are no dependencies on other roles, but a recommended setup
includes:

 * nginx (I use geerlingguy.nginx)
 * PostgreSQL
 * Redis


Example Playbook
----------------

After installing a database server and creating the database etc.:

    - hosts: servers
      roles:
         - { role: on.gitea, gitea_version: 1.7.4 }

License
-------

Licensed under the LGPLv3+, see here:

https://www.gnu.org/licenses/lgpl-3.0.txt


Author Information
------------------

Toni Mueller <support@oeko.net>
(c) 2017-2019

