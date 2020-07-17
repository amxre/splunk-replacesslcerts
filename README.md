# splunk-replacesslcerts
This is a crude Ansible script to replace SSL certs in any environment. Needs some love but I'll get it there. Feel free to make pulls

## populate your hosts file

#{Optional} But Recommended
Fetch server.conf for all your servers and lay out a game plan, tweak your script as needed to match it using this script
fetch-rootca
fetch-serverconf
fetch-webconf

## Create this on the server running the ansible script
/tmp/hostname

## Add your certs to 
/tmp/hostname

## Add your new server.conf with splunkd and splunk web configs to
/tmp/hostname


## Run scripts in the following order

0-backup - backs up existing certs to same directory {e.g. server.conf.bak.ansible}
1-upload - uploads scripts in /tmp/<hostname> to /opt/splunk/etc/auth/new_cert/
2a-configureserver - Configures splunkd cert configs with desired parameters
2b-configureweb - COnfigures splunk web cert configs with desired parameters

## Uh Oh {Rollback procedure}
rollback.yaml


