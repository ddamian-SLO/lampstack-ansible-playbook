# LAMP Stack Ansible Playbook
Work in progress

## Summary
The main purpose of this Playbook is to create a complete LAMP stack from scratch. It will utilize Apache and PHP FPM, create users, create vHost entries, and create databases

In the future, I plan to use the playbook to install WordPress for each site, which is the reason wp-cli is downloaded under the "common" role. 

## Roles
**Apache** - The apache role will install Apache2, enable modules, and copy over vhost entries, edit them from the default site.conf template, then enable them.

**Common** - Installs pre-req packages

**MySQL** - Handles installation of MariaDB/MySQL, sets the root password, and sets up databases. Once a wordpress role is made, database creation will be handled on that role.

**PHP** - Install PHP FPM and related PHP packages, then create FPM pools for each site defined in vars.yml.

**User** - Create website users and their directories they'll store website files on. 