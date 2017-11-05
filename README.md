## Docker XNAT build for development and test environments.

--Pre-requists:
   1) Linux host(whatever flavour you wish you use).
   2) Docker CE installed.
   2) Docker Compose installed.

--Building base XNAT build in Docker container:

   1) Download this git repository "git pull <URL to .git>
   2) Browse to the downloaded git repository 
   3) Edit docker-compose.yml file and chnage folder paths under VOLUME.
   3) Create folder "webapps" and  download latest xnat.war 
   "wget --no-cookies https://bintray.com/nrgxnat/applications/download_file?file_path=xnat-web-1.7.4.war -O webapps/xnat.war"
   4) Build XNAT running "docker-compose up -d" from within the pulled git repository.

Your XNAT will be up and running in a minute or two.

--To check Progress of XNAT build run "docker-compose logs -f --tail=10 xnat-web"

--Software Inventory 
   1) Tomcat + XNAT: The XNAT web application
   2) Postgres: The XNAT database
   3) nginx: Web proxy sitting in front of XNAT

--------------
To login to XNAT browse to "FQDN" or "IP" address of the underlying host/server followed by "xnat" Example: xnat-dev.mydomain.com/xnat or 10.0.1.12/xnat

Username: admin
password: admin 

Thanks to NrgXnat!.
