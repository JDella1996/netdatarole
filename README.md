Netdatarole
=========

This role is designed to deploy multipe Netdata instances to be scraped. 

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------
netdata_installer_url: https://my-netdata.io/kickstart.sh 
Has the url for the installer script

netdata_installer: "kickstart.sh"
Has the name of the installer script

proxy_env:
  https_proxy: ""
If you are using a proxy

download_dir: "/tmp/netdata"
The download location

netdata_install_path: "/etc/netdata" 
The install location

netdata_user_uid: 4321
Creates a user with a set UID

log_dir: "/export/netdata"
The location of logs

netdata_hostname: "{{hostvars[inventory_hostname]['ansible_hostname']}}"
The name of the host

configure_netdata_collectors: false
Configures the collectors

remove_existing_install: false
Remove existing installs.

