# geoserver
module for deploying geoserver forked from https://github.com/camptocamp/puppet-geoserver.

This is still a WIP.

This module will create a user and an instance of tomcat to host geoserver and deploy the geoserver with basic configuration. You have to provide proper hiera variables:
```
data_dir - this should be /opt/geoserver/data
cache_dir - this should be /opt/geoserver/cache
rolename
username
password
roles
datastore_name
llc_local_authority_api_db_host
llc_local_authority_api_db_name
llc_local_authority_api_db_user
llc_local_authority_api_db_pass

connector_port - default 8080
```

The module will get the geoserver.war file from https://downloads.sourceforge.net/ and install it to `/srv/tomcat/geoserver/webapps/geoserver.war`.




dependancies:
https://github.com/camptocamp/puppet-tomcat
