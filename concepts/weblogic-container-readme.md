# Run WebLogic in a docker container
This repository contains sample Docker configurations to facilitate installation, configuration, and environment setup - https://github.com/oracle/docker-images/tree/main/OracleWebLogic

* Steps to set it up is best explained here - https://redthunder.blog/2017/05/08/building-a-docker-image-for-weblogic-12-2-1-2-with-medrec-app/

## Start the WebLogic Server (WLS) Administration Console
```bash
# Command to run the WebLogic Server (WLS) Administration Console: 
docker run -d -p 7001:7001 -p 9002:9002  -v /mnt/c/abhinab/work/github/docker-images/OracleWebLogic/dockerfiles/14.1.1.0/properties:/u01/oracle/properties -e ADMINISTRATION_PORT_ENABLED=true -e DOMAIN_NAME=docker_domain -e ADMIN_NAME=docker-AdminServer oracle/weblogic:14.1.1.0-developer-8

# The console is up on localhost if using WSL
https://localhost:9002/console

# If not using WSL, then get the IP address 
docker inspect --format '{{.NetworkSettings.IPAddress}}' <container-name>
# In your browser, go to: 
https://xxx.xx.x.x:9002/console
```

> Username: myweblogicuser Password: welcome1

## Run MedRec sample application
[Medrec WLS sample application](https://github.com/oracle/docker-images/tree/main/OracleWebLogic/samples/12212-medrec)

Download the file [fmw_14.1.1.0.0_wls_supplemental_quick_Disk1_1of1.zip](https://www.oracle.com/middleware/technologies/weblogic-server-downloads.html) & place it in the folder `docker-images/OracleWebLogic/samples/12212-medrec` next to the dockerfile.

Update the dockerfile with the following changes:
* Update the base image to `oracle/weblogic:14.1.1.0-developer-8`
* Update the below Environment variables to have the correct version i.e. `14.1.1.0.0`
    * FMW_PKG 
    * FMW_JAR

```bash
# Build the sample application on top of WLS
docker build -t 14110-medrec .
# To start the Admin Server, run:
docker run -d -p 7011:7011 14110-medrec
# When you run the container a MedRec domain is created and the server started. To access the MedRec application, go to:
http://localhost:7011/medrec
# To access the WebLogic admin console, go to:
http://localhost:7011/console
```

> Username: weblogic Password: welcome1