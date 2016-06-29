# ownCloud
Create and onwCloud server in CLC cloud

## Parameters
* ocroot # ex: /datatemp  
* ocpath # ex: /datatemp/www/owncloud
* htuser # ex: www-data
* htgroup # ex: www-data
* mysqlpass # ex: abc123!@#
* permpath # ex: /datatemp/www/owncloud

### DESCRIPTION:
This playbook will provision an Ubuntu 14.04 server the Centurylink Cloud and deploys a working instance of ownCloud to it.
The high level tasks are as follows:
* provision a group and server
* install and harden MySQL and create the owncloud database
* install apache, postfix and some php packages
* make some dorectory structures, set some premissions & ownership and copy some config files to the server
* configure apache and postfix
