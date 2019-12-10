# Magento-2.3 Elasticsearch 6.0.1 docker-compose

##1. Prerequisites
    Install docker-compose `https://docs.docker.com/compose/install/`
    
##2. Using:
    Run `docker-compose up` in folder where this repository is cloned.

##3. Magento 2:
    ###Pre-install script
    bin/magento setup:install --es-hosts="elasticsearch:9200" --es-user="username" --es-pass="changeme"
    
    ###Post-install script
    magento config:set catalog/search/engine 'elasticsearch5'
    magento config:set catalog/search/elasticsearch6_server_hostname 'localhost'
    magento config:set catalog/search/elasticsearch6_server_port '9200'
    magento config:set catalog/search/elasticsearch6_index_prefix 'magento2'
    magento config:set catalog/search/elasticsearch6_enable_auth '0'
    magento config:set catalog/search/elasticsearch6_server_timeout '15'
    