# README.md
# Ansible Role: mats116.pandorafms-server

An Ansible role that installs Pandora FMS Server on **Ubuntu 14.04 LTS**

## Requirements

none

## Role Variables

Available variables are listed below, along with default values:

```yaml
pandora_version: ""

pandora_nginx_accesslog: /var/log/nginx/pandora-access.log

pandora_mysql_host: localhost
pandora_mysql_database: pandora
pandora_mysql_user: pandora
pandora_mysql_password: pandora
```

## Dependencies

- [mats116.nginx](https://galaxy.ansible.com/detail#/role/6198) - Installer of Nginx
- [mats116.php5-fpm](https://galaxy.ansible.com/detail#/role/6238) - Installer of php-fpm
- [mats116.mariadb-server](https://galaxy.ansible.com/detail#/role/6199) - Installer of MariaDB Server (MySQL)
 - `when "pandora_mysql_host == 'localhost'"`

## Example Playbook

```yaml
- hosts: pandorafms-server
  roles:
    - role: mats116.pandorafms-server
```

## License

MIT
