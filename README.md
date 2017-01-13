# nginx reverse proxy
Ansible role for installing nginx reverse proxy
Author: Bojan Dimitrovski, May 6th 2016.

# Usage

Run **vagrant up**
Optional: **vagrant up --provider=parallels** or **vagrant up --provider=virtualbox**

The Vagrantfile will provision a Debian machine and install nginx on it. Then, it will deploy the template file for the reverse nginx proxy with all requested parameters.

If you run into any issues with provisioning the Debian machine, use a ready-made box from here: http://www.vagrantbox.es/
