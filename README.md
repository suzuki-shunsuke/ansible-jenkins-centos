ansible-jenkins-centos
======================

ansible role to install Jenkins on CentOS

https://galaxy.ansible.com/suzuki-shunsuke/jenkins-centos/

Requirements
------------

Nothing.

Role Variables
--------------

* jenkins_jdk: JDK yum package name. The default is "java-1.8.0-openjdk". If you don't want to install jdk by yum, set "no"
* jenkins_state: jenkins service state. The default is "no", which means don't change jenkins service state.
* jenins_enabled: Whether the service should start on boot. In default don't change jenkins service state.

Dependencies
------------

Nothing.

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
  - role: suzuki-shunsuke.jenkins-centos
    jenkins_jdk: no
    jenkins_state: started
    jenkins_enabled: yes
```

License
-------

MIT
