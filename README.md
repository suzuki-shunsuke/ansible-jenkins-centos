# ansible-jenkins-centos

ansible role to install Jenkins on CentOS

https://galaxy.ansible.com/suzuki-shunsuke/jenkins-centos/

## Requirements

Nothing.

## Role Variables

name | required | default | description
--- | --- | --- | ---
jenkins_jdk | no | java-1.8.0-openjdk | JDK yum package name. If you don't want to install jdk by yum, set "no"
jenkins_state | no | | jenkins service state. The default is "no", which means don't change jenkins service state
jenins_enabled | no | | Whether the service should start on boot. By default don't change jenkins service state
jenins_port | no | | `JENKINS_PORT` in `/etc/sysconfig/jenkins`
jenkins_listen_address | no | | `JENKINS_LISTEN_ADDRESS` in `/etc/sysconfig/jenkins`
jenkins_args | no | | `JENKINS_ARGS` in `/etc/sysconfig/jenkins`

## Dependencies

Nothing.

## Example Playbook

```yaml
- hosts: servers
  roles:
  - role: suzuki-shunsuke.jenkins-centos
    jenkins_jdk: no
    jenkins_state: started
    jenkins_enabled: yes
    jenkins_port: 5000
    jenkins_listen_address: 127.0.0.1
    jenkins_args: "--sessionTimeout=1440"
    become: yes
```

## Change Log

See [CHANGELOG.md](CHANGELOG.md).

## License

[MIT](LICENSE)
