# Installation Guide for Evergreen ILS

## Goal: Use Evergreen ILS to manage Aim High's summer program books and personal Central Office library to use with barcode scanner.

### Resources
Read more about [Evergreen, an Open Source Integrated Library System](https://evergreen-ils.org/about-us/)

[Server Requirements](http://docs.evergreen-ils.org/reorg/3.2/command_line_admin/_system_requirements.html#_server_minimum_requirements)
[Staff Client Requirements](http://docs.evergreen-ils.org/reorg/3.2/command_line_admin/_staff_client_requirements.html)

[Installing Prerequisites](http://docs.evergreen-ils.org/reorg/3.2/command_line_admin/_installing_prerequisites.html)
Prerequisites:
- [VirtualBox](https://www.virtualbox.org/) or [VMWare](https://www.vmware.com/)
- [Ubuntu server (18.04)](https://ubuntu.com/download/server)
- PostgreSQL (11)
- OpenSRF (3.1.1)

I'll be using VMWare for this installation.

###### Accounts
Local Ubuntu account: erica

## [Installing Prerequisites](http://docs.evergreen-ils.org/reorg/3.2/command_line_admin/_installing_prerequisites.html)
### [Installing OpenSRF](https://evergreen-ils.org/documentation/install/OpenSRF/README_3_2_0.html)

1. As local Ubuntu user, get a stable tarball from https://evergreen-ils.org/opensrf-downloads/ and unpack tarball.
'''
wget https://evergreen-ils.org/downloads/opensrf-3.2.0.tar.gz
tar xvf opensrf-3.2.0.tar.gz
cd opensrf-3.2.0/
'''

2. Install OpenSRF using Makefile.install prerequisite installer as root
'''
sudo apt-get install make
make -f src/extras/Makefile.install ubuntu-bionic
'''
note: Makefile.install will only run on ubuntu-bionic and ubuntu-xenial

note: If you get error where C compiler was not found in $PATH, run the following command:
'''
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install build-essential
'''

If you get "configure: error: could not determine apache version number":
'''
sudo apt-get install apache2...nope will try again
'''
left off on 5. Configuration and compilation instructions
(https://evergreen-ils.org/documentation/install/OpenSRF/README_3_2_0.html)
