# modsecwordpress
Module security and OWASP rules with wordpress on docker


#Modsecurity 
from repository

#wordpress
https://hub.docker.com/_/wordpress/

#OWASP mod sec rules
https://github.com/SpiderLabs/owasp-modsecurity-crs

#basic usage
docker run --name mysql -e MYSQL_ROOT_PASSWORD=test mysql
docker run --name test --link mysql:mysql -p 80:80 -d ifpr/modsecwordpress
