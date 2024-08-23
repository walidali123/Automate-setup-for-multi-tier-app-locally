# Vagrant Multi-VM Setup

This project sets up a multi-VM environment using Vagrant and VirtualBox. The environment consists of five virtual machines: a database server, a Memcache server, a RabbitMQ server, a Tomcat application server, and an Nginx web server. Each VM is configured with specific roles and provisions using shell scripts.

## Prerequisites

- [Vagrant](https://www.vagrantup.com/downloads)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- Vagrant plugins:
  - `vagrant-hostmanager`: Manage host entries for the VMs

To install the necessary plugins, run:

```sh
vagrant plugin install vagrant-hostmanager

Setup
Clone this repository and navigate to the project directory:

sh
Copy code
git clone <repository_url>
cd <project_directory>
Configuration
The Vagrantfile is configured to create the following VMs:

DB VM
Name: db01
Box: eurolinux-vagrant/centos-stream-9
Box Version: 9.0.43
Hostname: db01
IP Address: 192.168.56.15
Memory: 600 MB
Provisioning Script: mysql.sh
Memcache VM
Name: mc01
Box: eurolinux-vagrant/centos-stream-9
Box Version: 9.0.43
Hostname: mc01
IP Address: 192.168.56.14
Memory: 600 MB
Provisioning Script: memcache.sh
RabbitMQ VM
Name: rmq01
Box: eurolinux-vagrant/centos-stream-9
Box Version: 9.0.43
Hostname: rmq01
IP Address: 192.168.56.16
Memory: 600 MB
Provisioning Script: rabbitmq.sh
Tomcat VM
Name: app01
Box: eurolinux-vagrant/centos-stream-9
Box Version: 9.0.43
Hostname: app01
IP Address: 192.168.56.12
Memory: 800 MB
Provisioning Script: tomcat.sh
Nginx VM
Name: web01
Box: ubuntu/jammy64
Hostname: web01
IP Address: 192.168.56.11
Memory: 800 MB
Provisioning Script: nginx.sh
Usage
To start the VMs, navigate to the project directory and run:

sh
Copy code
vagrant up
This command will provision and boot up all the VMs defined in the Vagrantfile.

Accessing the VMs
You can SSH into any of the VMs using:

sh
Copy code
vagrant ssh <vm_name>
Replace <vm_name> with one of the following: db01, mc01, rmq01, app01, or web01.

Stopping the VMs
To halt the VMs, run:

sh
Copy code
vagrant halt
Destroying the VMs
If you need to destroy the VMs and clean up the environment, run:

sh
Copy code
vagrant destroy -f
License
This project is licensed under the MIT License. See the LICENSE file for details.

javascript
Copy code

Replace `<repository_url>` and `<project_directory>` with your actual repository URL and project directory name.








