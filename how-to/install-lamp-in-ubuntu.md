---
title: How to Install LAMP in Ubuntu
breadcrumb: install lamp
excerpt: The following tutorial presumes you understand what a LAMP Server is, how to work a website from the back end. It also expect experience running other Basic Terminal Commands.
---

The following tutorial presumes you understand what a LAMP Server is, how to work a website from the back end. It also expect experience running other Basic Terminal Commands.

There is also an [excellent article on Digital Ocean](https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-20-04) that may be of more relevance if you are working on a remote or public facing server.

## 1. Install Apache

To install Apache you must install the Metapackage <span class="box">apache2</span>. This can be done by searching for and installing in the Software Centre, or by running the following command.

```bash
sudo apt install apache2
```

## 2. Install MySQL

To install MySQL you must install the Metapackage <span class="box">mysql-server</span>. This can be done by searching for and installing in the Software Centre, or by running the following command.

```bash
sudo apt install mysql-server
```

## 3. Install PHP

PHP requires a few packages to work as you expect, so we recommend the following command.

```bash
sudo apt install php php-mysql libapache2-mod-php
```

## 4. Restart Apache Server

Your server should restart Apache automatically after the installation of both MySQL and PHP. If it doesn't, execute this command:

```bash
sudo service apache2 restart
```

## 5. Check Apache

Open a web browser and navigate to <a href="http://localhost/">http://localhost/</a>. You should see a message saying <span class="box">It works!</span>

## 6. Check PHP

You can check your PHP by executing any PHP file from within <span class="box">/var/www/</span>. Alternatively you can execute the  following command, which will make PHP run the code without the need for creating a file .

```bash
php -r 'echo &quot;\n\nYour PHP installation is working fine.\n\n\n&quot;;'
```

## 7. Secure MySQL

We recommend you run the guided setup for securing MySQL, but this may be unecessary in a development environment.

```bash
sudo mysql_secure_installation
```

## Congratulations, you have just Installed a Ubuntu LAMP Server!
