debops-contrib.eset_server
==========================

This role installs the `ESET Remote Administrator`__ server (backend). You can
read the `installation instructions (PDF)`__ for an overview of the
installation process.

.. __: https://www.eset.com/int/business/remote-management/remote-administrator/
.. __: http://download.eset.com/manuals/eset_era_63_era_install_enu.pdf

You can find the corresponding playbook in the
``ansible/playbooks/service/eset_server.yml`` file. The role uses Ansible roles
from the DebOps project as dependencies.

The ERA server uses MySQL as a database backend. You can use the
``debops.mariadb_server`` Ansible role to configure a suitable server. ERA
requires additional database server configuration:

.. code-block:: yaml

   mariadb_server__options:

     - section: 'mysqld'
       options:
         'innodb_log_file_size': '200M'
         'max_allowed_packet': '64M'

   mariadb_server__flavor: 'mysql'
