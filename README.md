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

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

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

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

Licensed under the LGPLv3+, see here:

https://www.gnu.org/licenses/lgpl-3.0.txt


Author Information
------------------

Toni Mueller <support@oeko.net>
(c) 2017-2018

