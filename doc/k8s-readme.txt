1. env. variables to be set:
---------
MYSQL_HOST=35.227.18.222
MYSQL_DB=uaa
MYSQL_USER=doctor
MYSQL_PWD=<**>
MYSQL_SSL_SERVER_CERT=/uaa/credentials/server-ca.pem
MYSQL_SSL_KEYSTORE=/uaa/credentials/gcp-mysql.jks
MYSQL_SSL_KEYSTORE_PASSWD=<**>
MYSQL_SSL_KEY_PASSWD=<**>


2. files stored in secured bucket should be dowloaded :
       server-ca.pem, gcp-mysql.jks, uaa-mysql-asgard.yml:
       
    environment:
    - UAA_CONFIG_FILE=/uaa/config/uaa-mysql-asgard.yml
    volumes:
    - /Users/alexchervin/git/docker-env/credentials:/uaa/credentials
    - /Users/alexchervin/git/docker-env/config/:/uaa/config
