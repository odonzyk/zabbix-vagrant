# Vagrant for Zabbix

This Vagrant configuration can be used for quick testing purposes of Zabbix infrastructure.

# Requirements

* [VirtualBox](https://www.virtualbox.org/)
* [Vagrant](https://www.vagrantup.com/)

# Usage

Just use Vagrant to start Zabbix server. From inside directory where you cloned this repository run the following command:
```
vagrant up
```

After machine finished provisioning you will be able access web interface using **[http://localhost:8080/](http://localhost:8080)** with default credentials:
  * login: **Admin**
  * password: **zabbix**

### Change ports

If you need to change ports on your host just edit Vagrantfile and replace *forwarded_port* setting.

# Technical details

The installed software is:

|component|version|
|---|---|
|Ubuntu|**18.04.3 LTS** (bionic)|
|Mysql|**Ver 15.1 Distrib 10.1.43-MariaDB 9.5.x**|
|Zabbix server|**4.0.15**|
|Zabbix agent|**4.0.15**|

Commands used in provision script are based on official documentation:

* [Installation from packages → Debian/Ubuntu](https://www.zabbix.com/documentation/4.0/manual/installation/install_from_packages/debian_ubuntu)
* [Installation from sources → Installing frontend](https://www.zabbix.com/documentation/4.0/manual/installation/install#installing_frontend)


![alt text](img/zabbix.png "Screenshoot Zabbix")
