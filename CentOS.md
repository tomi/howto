# CentOS

## Administration

### Package manager (yum)

* Install a package `yum install <package name>`
* Remove a package `yum remove <package name>`
* Update a package `yum update <package name>`

* Check for updates `yum check-update`
* Install updates `yum update`

### Manage systemd services and units (systemctl)

See also [this excellent DigitalOcean article on the topic](https://www.digitalocean.com/community/tutorials/how-to-use-systemctl-to-manage-systemd-services-and-units)

* Start a service `sudo systemctl start <service name>.service`
* Stop a service `sudo systemctl stop <service name>.service`
* Restart a service `sudo systemctl restart <service name>.service`

* Enable a service `sudo systemctl enable <service name>.service`
* Disable a service `sudo systemctl disable <service name>.service`

* Check status of a service `systemctl status <service name>.service`