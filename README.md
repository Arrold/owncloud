# ownCloud
Create and ownCloud server in CLC cloud

## Parameters
* owncloud_root # ex: /data_oc/www
* htaccess_user # ex: www-data
* htaccess_group # ex: www-data
* mysql_root_pass # ex: "abc123!@#"

### DESCRIPTION:
This playbook is designed to be called by Runner and will provision an Ubuntu 14.04 server in CenturyLink Cloud and deploys a working instance of ownCloud to it.
The high level tasks are as follows:
* provision a group and server
* install and harden MySQL and create the owncloud database
* install apache, postfix and some php packages
* make some directory structures, set some permissions & ownership and copy some config files to the server
* configure apache and postfix

### NOTES:
Because ownCloud is a sort of private dropbox it's probable that a disk (partition) will need to be added to the instance to serve as storage, in the examples given this should be added to /data.
Once the play is successful, add a disk, move the contents of /datatemp to /data, sign in to your VPN then hit the private IP at https://aa.bb.cc.dd/owncloud

### PREREQUISITES
You must have a CenturyLink Cloud account to be able to use Runner

### ADDITIONAL STEPS
Once the Server has been configured
