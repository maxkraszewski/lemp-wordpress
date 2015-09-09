# LEMP Vagrant Ansible Wordpress

Create a local environment for quickly test Wordpress websites.

Includes:
- Ubuntu 14.04 Trusty
- Nginx 1.4.6
- PHP 5.6
- MySQL 5.5
- Wordpress 4.3

## Requirements
- [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
- [Vagrant](http://www.vagrantup.com/downloads.html)
- [Ansible](http://docs.ansible.com/intro_installation.html)

## Installation
1. Install Virtualbox, Vagrant and Ansible
2. Clone repository into a desired folder
```
git clone https://github.com/minimalart/lemp-wordpress.git
```

3. Move to repository folder
```
cd lemp-wordpress
```
4. (Optional) Customize local ip

  If you use the default box, no configuration should be required to get up and running.
  However if you want to use an IP address other than ```192.168.100.101```, replace that address with the one you wish to use in `Vagrantfile (line 8)`
5. Edit your /etc/hosts:

  ```
  192.168.100.101 wordpress.local
  ```
6. Run the commands below:
  ```
  vagrant up
  ```
  The setup will take some time to finish. In the meantime, you can have a [sword fight](http://xkcd.com/303/).

7. Browse to [http://wordpress.local](http://wordpress.local) and enjoy.
8. You can login to the WP Admin Panel in [http://wordpress.local/wp-admin](http://wordpress.local/wp-admin) with user: ```wpadmin``` and password: ```wppass```

---
#### Tips and Hints:

* All users and passwords for accesing WP Admin Panel are located in ***ansible/settings.yml*** file.
* You can ```ssh```into the VM with ```vagrant ssh```command, with no password.
* ***WP-CLI*** is installed, so you can run ```wp``` commands as described in [http://wp-cli.org/](http://wp-cli.org/)
