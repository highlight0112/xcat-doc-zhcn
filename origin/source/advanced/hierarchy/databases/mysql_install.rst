Install MySQL/MariaDB
=====================

The MySQL database is supported by xCAT since xCAT 2.1.  MariaDB is a fork of the MySQL project which was released around 2009 and is a drop-in replacement for MySQL.  MariaDB support within xCAT started in version 2.8.5 and is currently fully supported moving forward.

+------------+------------+------------+
| Database   | MySQL      | MariaDB    |
+============+============+============+
| xCAT 2.1+  | Yes        | No         |
+------------+------------+------------+
| xCAT 2.8.5 | Yes        | RHEL 7     |
+------------+------------+------------+
| xCAT 2.9   | Yes        | SLES 12    |
+------------+------------+------------+
| xCAT 2.10+ | Yes        | Yes        |
+------------+------------+------------+

MySQL/MariaDB packages are shipped as part of most Linux Distributions.


Red Hat Enterprise Linux
------------------------

* For RHEL 6 and prior, MySQL is shipped. Using ``yum``, ensure that the following packages are installed on the management node: ::

       perl-DBD-MySQL*
       mysql-server-5.*
       mysql-5.*
       mysql-connector-odbc-*

* For RHEL 7, MariaDB is shipped. Using ``yum``, ensure that the following packages are installed on the management node: ::

       mariadb-server-5.*
       mariadb-5.*
       perl-DBD-MySQL*
       mysql-connector-odbc-*

* For RHEL 8, MariaDB is shipped. Using ``dnf``, ensure that the following packages are installed on the management node: ::

       mariadb-server-10.*
       mariadb-10.*
       perl-DBD-MySQL*
       mariadb-connector-odbc-*

Suse Linux Enterprise Server
----------------------------

* MySQL - Using ``zypper``, ensure that the following packages are installed on the management node: ::

       mysql-client-5*
       libmysqlclient_r15*
       libqt4-sql-mysql-4*
       libmysqlclient15-5*
       perl-DBD-mysql-4*
       mysql-5*

* MariaDB - Using ``zypper``, ensure that the following packages are installed on the management node: ::

       mariadb-client-10.*
       mariadb-10.*
       mariadb-errormessages-10.*
       libqt4-sql-mysql-*
       libmysqlclient18-*
       perl-DBD-mysql-*

* For SLE15, MariaDB is shipped. Using ``zypper``, ensure that the following packages are installed on the management node: ::

       mariadb
       mariadb-client
       mariadb-errormessages
       perl-DBD-mysql
       libmariadb-devel
       mariadb-tools
       libmariadb_plugins


Debian/Ubuntu
-------------

* MySQL - Using ``apt-get``, ensure that the following packages are installed on the management node: ::

        mysql-server
        mysql-common
        libdbd-mysql-perl
        libmysqlclient*
        mysql-client-5*
        mysql-client-core-5*
        mysql-server-5*
        mysql-server-core-5*

* MariaDB - Using ``apt-get``, ensure that the following packages are installed on the management node. ``apt-get install mariadb-server`` will pull in all required packages. For Ubuntu 16.04, it no longer required ``libmariadbclient18``. ::

        libmariadbclient18
        mariadb-client
        mariadb-common
        mariadb-server
