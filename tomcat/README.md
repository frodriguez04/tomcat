Apache Tomcat
=============

This role installs Apache Tomcat v 9.0.43

Requirements
------------

This role uses the Java role

Role Variables
--------------

Please refer to the defaults/main.yml for the variables that can be set

Dependencies
------------

None

Example Playbook
----------------

```
- name: Install Tomcat
  hosts: all
  tasks:
    - name: "Include tomcat"
      include_role:
        name: "tomcat"
```

For deploying a war file to an existing installation of Tomcat:

```
- name: Deploy WAR
  hosts: all
  vars:
    tcat_deployment_url: https://tomcat.apache.org/tomcat-9.0-doc/appdev/sample/sample.war
    tcat_deploy: true
    tcat_install: false
  tasks:
    - name: "Include tomcat"
      include_role:
        name: "tomcat"

```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
