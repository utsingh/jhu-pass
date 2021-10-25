./sp/2.6.1/etc-httpd/conf.d/sp.conf:83:    ProxyPass /es http://elasticsearch:9200/pass/_search
./sp/2.6.1/etc-httpd/conf.d/sp.conf:84:    ProxyPassReverse /es http://elasticsearch:9200/pass/_search
./.harvard_env:53:PASS_ELASTICSEARCH_URL=http://elasticsearch:9200
./.harvard_env:69:# Elasticsearch config
./.harvard_env:78:PI_ES_BASE=http://elasticsearch:9200/
./.harvard_env:79:PI_ES_INDEX=http://elasticsearch:9200/pass/
./README.md:64:  - PASS_ELASTICSEARCH_URL: URL used for elasticsearch queries
./README.md:143:- PASS_ELASTICSEARCH_URL
./README.md:144:- PASS_ELASTICSEARCH_LIMIT
./README.md:183:### Elasticsearch-related variables
./README.md:185:  - ES_PORT: the port that Elasticsearch is exposed on, defaults to `9200`
./README.md:194:  - PI_ES_BASE: URL to base of Elasticsearch. Used to test if it is up.
./README.md:195:  - PI_ES_INDEX: URL to Elasticsearch index where Fedora resources will be indexed.
./README.md:196:  - PI_ES_CONFIG: URL to Elasticsearch index where Fedora resources will be indexed.
./README.md:201:  - PI_MAX_ATTEMPTS: set the max attempts to contact Elasticsearch and Fedora (default: 20)
./README.md:255:- `PASS_ELASTICSEARCH_URL` (`pass.elasticsearch.url`): base URL of the ElasticSearch API for the PASS index (`http://${es.host:localhost}:${es.port:9200}/pass`)
./README.md:256:- `PASS_ELASTICSEARCH_LIMIT` (`pass.elasticsearch.limit`): number of records retrieved by default when performing a search of the index (`100`)
./.env:61:PASS_ELASTICSEARCH_URL=http://elasticsearch:9200
./.env:78:# Elasticsearch config
./.env:87:PI_ES_BASE=http://elasticsearch:9200/
./.env:88:PI_ES_INDEX=http://elasticsearch:9200/pass/
./docker-compose.yml:166:  elasticsearch:
./docker-compose.yml:167:    #image: docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3@sha256:ccfad77c0731c010e6ff8c43b4ab50f5ce90c0fa4e65846530779c5c6707c20a
./docker-compose.yml:168:    image: docker.elastic.co/elasticsearch/elasticsearch:7.15.1
./docker-compose.yml:169:    container_name: elasticsearch
./docker-compose.yml:180:      - passdata:/usr/share/elasticsearch/data
./harvard.yml:164:  elasticsearch:
./harvard.yml:165:    image: docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3@sha256:ccfad77c0731c010e6ff8c43b4ab50f5ce90c0fa4e65846530779c5c6707c20a
./harvard.yml:166:    container_name: elasticsearch
./harvard.yml:177:      - passdata-harvard:/usr/share/elasticsearch/data
./notification-services/0.1.0-3.4/Dockerfile:8:    ES_HOST=${ES_HOST:-elasticsearch} \
./notification-services/0.1.0-3.4/Dockerfile:12:    PASS_ELASTICSEARCH_LIMIT=${PASS_ELASTICSEARCH_LIMIT:-100} \
./indexer/0.0.18-SNAPSHOT/wait_and_start.sh:49:    echo "Waiting for response from Elasticsearch via ${CMD}"
./indexer/0.0.18-SNAPSHOT/wait_and_start.sh:71:    echo "Elasticsearch is up"
./httpd-proxy/etc-httpd/conf.d/httpd.conf:74:    # Allow the pass Elasticsearch index to be searched as /es
./httpd-proxy/etc-httpd/conf.d/httpd.conf:75:    # Convert private Fedora URIs returned by Elasticsearch to public URIs.
./httpd-proxy/var-www-html/index.html:14:        <li><a href="/es/">Elasticsearch</a></li>
