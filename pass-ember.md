# pass-ember
*extensive use of ElasticSearch for autocomplete, queries, etc*

### APP

#### adapter provides an adapter from fedora into elasticsearch.
- ./app/adapters/application.js:9:  elasticsearchURI = ENV.fedora.elasticsearch;

#### Routes helps store the results returned from ES.
- ./app/routes/dashboard.js:22:    let approvalResults = await this.ajax.post(ENV.fedora.elasticsearch, {
- ./app/routes/dashboard.js:38:    let editsResults = await this.ajax.post(ENV.fedora.elasticsearch, {

#### Services have a bunch of different kinds of services like autocomplete, search-helper, etc.

1. Search Helper: service to help other components that rely on ES.
- ./app/services/search-helper.js:6: * This service can be referenced by components that rely on Elasticsearch query results
- ./app/services/search-helper.js:74:   * Wait for Elasticsearch to be reindexed with the given value.

2. Autocomplete: provides autocomplete feature during search on UI. Does a complicated elasticsearch query suggesting how to complete the prefix of something. Happens when you're trying to find an existing publication.
- ./app/services/autocomplete.js:6: * Service designed to hit the Elasticsearch autocomplete service to get suggestions
- ./app/services/autocomplete.js:23:    return ENV.fedora.elasticsearch;
- ./app/services/autocomplete.js:112:   * Adapt Elasticsearch results to a flat array.
- ./app/services/autocomplete.js:115:   * 'response.suggest' is where Elasticsearch sticks the autocomplete suggestions.
- ./app/services/autocomplete.js:122:   * @param {object} response response from Elasticsearch

### pass-ember client utilizes the fedora adapter to run queries on ES.


### Environment Configs

- ./config/environment.js:66:    elasticsearch: 'http://localhost:9200/pass/_search'
- ./config/environment.js:128:    ENV.fedora.elasticsearch = process.env.FEDORA_ADAPTER_ES;

### README

- ./README.md:10:Objects persisted to Fedora are automatically indexed by Elasticsearch. See- 

- ./README.md:12:Note that the indexing process is asynchronous. An object persisted to Fedora will not immediately be available in Elasticsearch.- 

- ./README.md:53:* Elasticsearch index search endpoint is at https://pass.local/es/- 

- ./README.md:68:and Elasticsearch are and generally will not need to be modified during development.- 

- ./README.md:70:In order to prevent an Authorization header being sent to Fedora and Elasticsearch,

### docker config variables
- ./.docker/.harvard_env:53:PASS_ELASTICSEARCH_URL=http://elasticsearch:9200
- ./.docker/.harvard_env:69:# Elasticsearch config
- ./.docker/.harvard_env:78:PI_ES_BASE=http://elasticsearch:9200/
- ./.docker/.harvard_env:79:PI_ES_INDEX=http://elasticsearch:9200/pass/
- ./.docker/.env:44:PASS_ELASTICSEARCH_URL=http://elasticsearch:9200
- ./.docker/.env:48:# Elasticsearch config
- ./.docker/.env:57:PI_ES_BASE=http://elasticsearch:9200/
- ./.docker/.env:58:PI_ES_INDEX=http://elasticsearch:9200/pass/
- ./.docker/docker-compose.yml:117:  elasticsearch:
- ./.docker/docker-compose.yml:118:    #image: docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3@sha256:ccfad77c0731c010e6ff8c43b4ab50f5ce90c0fa4e65846530779c5c6707c20a
- ./.docker/docker-compose.yml:119:    image: docker.elastic.co/elasticsearch/elasticsearch:7.15.1
- ./.docker/docker-compose.yml:120:    container_name: elasticsearch
- ./.docker/docker-compose.yml:131:      - passdata:/usr/share/elasticsearch/data
- ./.docker/harvard.yml:107:  elasticsearch:
- ./.docker/harvard.yml:108:    image: docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3@sha256:ccfad77c0731c010e6ff8c43b4ab50f5ce90c0fa4e65846530779c5c6707c20a
- ./.docker/harvard.yml:109:    container_name: elasticsearch
- ./.docker/harvard.yml:120:      - passdata-harvard:/usr/share/elasticsearch/data
