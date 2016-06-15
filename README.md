# modsecwordpress
modsecwordpress is a docker image that use wordpress image and import modsecurity module for apache and OWASP core rule set. (I'm not member of owasp core rule set project).

*this is a unofficial  docker image*

##OWASP ModSecurity Core Rule Set (CRS)

ModSecurity™ is a web application firewall engine that provides very little protection on its own. In order to become useful, ModSecurity™ must be configured with rules. In order to enable users to take full advantage of ModSecurity™ out of the box, Trustwave's SpiderLabs is sponsoring and maintaining a free certified rule set for the community. Unlike intrusion detection and prevention systems, which rely on signatures specific to known vulnerabilities, the OWASP ModSecurity Core Rule Set provides generic protection from unknown vulnerabilities often found in web applications, which are in most cases custom coded. The Core Rules are heavily commented to allow it to be used as a step-by-step deployment guide for ModSecurity™.

check the project : https://github.com/SpiderLabs/owasp-modsecurity-crs

##Use
docker run --name mysql -e MYSQL_ROOT_PASSWORD=123  -d mysql (start database first) <br />
docker run --name test --link mysql:mysql -p 80:80 -d ifpr/modsecwordpress

