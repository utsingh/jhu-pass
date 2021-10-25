# pass-ember
* extensive use of ElasticSearch for autocomplete, queries, etc *

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

### APP

#### adapter provides an adapter from fedora into elasticsearch.
./app/adapters/application.js:9:  elasticsearchURI = ENV.fedora.elasticsearch;

#### Routes helps store the results returned from ES.
./app/routes/dashboard.js:22:    let approvalResults = await this.ajax.post(ENV.fedora.elasticsearch, {
./app/routes/dashboard.js:38:    let editsResults = await this.ajax.post(ENV.fedora.elasticsearch, {

#### Services have a bunch of different kinds of services like autocomplete, search-helper, etc.

1. Search Helper: service to help other components that rely on ES.
./app/services/search-helper.js:6: * This service can be referenced by components that rely on Elasticsearch query results
./app/services/search-helper.js:74:   * Wait for Elasticsearch to be reindexed with the given value.

2. Autocomplete: provides autocomplete feature during search on UI. Does a complicated elasticsearch query suggesting how to complete the prefix of something. Happens when you're trying to find an existing publication.
./app/services/autocomplete.js:6: * Service designed to hit the Elasticsearch autocomplete service to get suggestions
./app/services/autocomplete.js:23:    return ENV.fedora.elasticsearch;
./app/services/autocomplete.js:112:   * Adapt Elasticsearch results to a flat array.
./app/services/autocomplete.js:115:   * 'response.suggest' is where Elasticsearch sticks the autocomplete suggestions.
./app/services/autocomplete.js:122:   * @param {object} response response from Elasticsearch

### Dist setup
- ./dist/index.html:10:<meta name="pass-ember/config/environment" - 

- ./dist/tests/index.html:11:<meta name="pass-ember/config/environment"- 

- ./dist/assets/pass-ember.js:33:      (0, _defineProperty2.default)((0, _assertThisInitialized2.default)(_this), "elasticsearchURI", _environment.default.fedora.elasticsearch);- 

- ./dist/assets/pass-ember.js:62:  //   elasticsearchURI: Absolute URI of Elasticsearch search service.- 

- ./dist/assets/pass-ember.js:130:    // Return a Promise which clears the specified Elasticsearch index- 

- ./dist/assets/pass-ember.js:131:    clearElasticsearch: function clearElasticsearch(index_url) {- 

- ./dist/assets/pass-ember.js:239:      which performs poorly, use Elasticsearch and return up to 100.- 

- ./dist/assets/pass-ember.js:256:    // Create an elasticsearch query that restricts the given query to the given type.- 

- ./dist/assets/pass-ember.js:258:    _create_elasticsearch_query: function _create_elasticsearch_query(query, jsonld_type) {- 

- ./dist/assets/pass-ember.js:287:    // Turn Elasticsearch results into a JSON-LD @graph suitable for normalizeResponse.- 

- ./dist/assets/pass-ember.js:289:    _parse_elasticsearch_result: function _parse_elasticsearch_result(result, info) {- 

- ./dist/assets/pass-ember.js:303:       Elasticsearch query.- 

- ./dist/assets/pass-ember.js:304:        The query must be a clause in the Elasticsearch query syntax or an object- 

- ./dist/assets/pass-ember.js:306:       See https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl.html.- 

- ./dist/assets/pass-ember.js:322:        Each property of a model object is available as an Elasticsearch field. The type of- 

- ./dist/assets/pass-ember.js:334:      var url = this.get('elasticsearchURI');- 

- ./dist/assets/pass-ember.js:343:      var data = this._create_elasticsearch_query(_query, jsonld_type);- 

- ./dist/assets/pass-ember.js:353:        return _this3._parse_elasticsearch_result(result, info);- 

- ./dist/assets/pass-ember.js:12908:;define("pass-ember/mirage/config", ["exports", "pass-ember/config/environment", "pass-ember/mirage/routes/users", "pass-ember/mirage/routes/elastic-search", "pass-ember/mirage/routes/journals", "pass-ember/mirage/routes/policies", "pass-ember/mirage/routes/funders", "pass-ember/mirage/routes/repositories", "pass-ember/mirage/routes/publications", "pass-ember/mirage/routes/submissions", "pass-ember/mirage/routes/submission-events", "pass-ember/mirage/routes/files", "pass-ember/mirage/routes/schemas", "pass-ember/mirage/routes/grants"], function (_exports, _environment, _users, _elasticSearch, _journals, _policies, _funders, _repositories, _publications, _submissions, _submissionEvents, _files, _schemas, _grants) {- 

- ./dist/assets/pass-ember.js:12919:    (0, _elasticSearch.default)(this);- 

- ./dist/assets/pass-ember.js:17833:                  return this.ajax.post(_environment.default.fedora.elasticsearch, {- 

- ./dist/assets/pass-ember.js:17869:                  return this.ajax.post(_environment.default.fedora.elasticsearch, {- 

- ./dist/assets/pass-ember.js:19717:   * Service designed to hit the Elasticsearch autocomplete service to get suggestions- 

- ./dist/assets/pass-ember.js:19849:       * Adapt Elasticsearch results to a flat array.- 

- ./dist/assets/pass-ember.js:19852:       * 'response.suggest' is where Elasticsearch sticks the autocomplete suggestions.- 

- ./dist/assets/pass-ember.js:19859:       * @param {object} response response from Elasticsearch- 

- ./dist/assets/pass-ember.js:19908:        return _environment.default.fedora.elasticsearch;- 

- ./dist/assets/pass-ember.js:21343:   * This service can be referenced by components that rely on Elasticsearch query results- 

- ./dist/assets/pass-ember.js:21426:       * Wait for Elasticsearch to be reindexed with the given value.- 

- ./dist/assets/pass-ember.map:1: PUT INTO pass-ember-75.md

### Environment Configs

- ./config/environment.js:66:    elasticsearch: 'http://localhost:9200/pass/_search'
- ./config/environment.js:128:    ENV.fedora.elasticsearch = process.env.FEDORA_ADAPTER_ES;

### README

- ./README.md:10:Objects persisted to Fedora are automatically indexed by Elasticsearch. See- 

- ./README.md:12:Note that the indexing process is asynchronous. An object persisted to Fedora will not immediately be available in Elasticsearch.- 

- ./README.md:53:* Elasticsearch index search endpoint is at https://pass.local/es/- 

- ./README.md:68:and Elasticsearch are and generally will not need to be modified during development.- 

- ./README.md:70:In order to prevent an Authorization header being sent to Fedora and Elasticsearch,
