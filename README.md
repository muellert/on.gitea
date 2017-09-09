Gitea
=====

Install Gitea

This role only deals with the configuration of Gitea, but does not deal
with downloading the software, nor with the configuration of any
ancilliary software, like a database server or webserer.

The role is intended to be used together with our other roles and the
general Ansible configuration framework we are using.


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


http_port:          web interface
http_urlhost:       web interface


ssh_host:           ssh configuration
ssh_port:           ssh configuration


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
(c) 2017

