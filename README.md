Ansible role for OracleJDK installation
=======================================

Installs OracleJDK 8 from WebUpd8 team's PPA (http://www.webupd8.org/2012/09/install-oracle-java-8-in-ubuntu-via-ppa.html).

Role Variables
--------------

* `oraclejdk_package`

  Name of package to install (default is `oracle-java8-installer`).

Actions role
------------

* adds `webupd8team/java` PPA
* updates `apt`'s cache
* accepts Oracle's license
* installs package

Example Playbook
----------------

Example of usage with default parameters:

    - hosts: localhost
      roles:
         - phpcoder.oraclejdk

Example of usage to install OracleJDK 7:

    - hosts: localhost
      roles:
         - { role: phpcoder.oraclejdk, oraclejdk_package: 'oracle-java7-installer' }

License
-------

GPLv2

Author Information
------------------

Slava Semushin <slava.semushin@gmail.com>
