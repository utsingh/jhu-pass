./app/adapters/fedora-jsonld.js:11://   elasticsearchURI: Absolute URI of Elasticsearch search service.
./app/adapters/fedora-jsonld.js:68:  // Return a Promise which clears the specified Elasticsearch index
./app/adapters/fedora-jsonld.js:69:  clearElasticsearch(index_url) {
./app/adapters/fedora-jsonld.js:178:    which performs poorly, use Elasticsearch and return up to 100.
./app/adapters/fedora-jsonld.js:192:  // Create an elasticsearch query that restricts the given query to the given type.
./app/adapters/fedora-jsonld.js:194:  _create_elasticsearch_query(query, jsonld_type) {
./app/adapters/fedora-jsonld.js:223:  // Turn Elasticsearch results into a JSON-LD @graph suitable for normalizeResponse.
./app/adapters/fedora-jsonld.js:225:  _parse_elasticsearch_result(result, info) {
./app/adapters/fedora-jsonld.js:237:    Elasticsearch query.
./app/adapters/fedora-jsonld.js:239:    The query must be a clause in the Elasticsearch query syntax or an object
./app/adapters/fedora-jsonld.js:241:    See https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl.html.
./app/adapters/fedora-jsonld.js:260:    Each property of a model object is available as an Elasticsearch field. The type of
./app/adapters/fedora-jsonld.js:272:    let url = this.get('elasticsearchURI');
./app/adapters/fedora-jsonld.js:282:    let data = this._create_elasticsearch_query(query, jsonld_type);
./app/adapters/fedora-jsonld.js:288:      return this._parse_elasticsearch_result(result, info);
./tests/unit/adapters/fedora-jsonld-test.js:23:      elasticsearch: 'http://localhost:9200/_search'
./tests/dummy/app/adapters/application.js:7:    this.set('elasticsearchURI', ENV.test.override ? ENV.test.override.elasticsearch : ENV.test.elasticsearch);
./tests/dummy/config/environment.js:53:    elasticsearch: 'http://localhost:9200/farm/_search',
./tests/dummy/config/environment.js:54:    elasticsearch_index: 'http://localhost:9200/farm/',
./tests/dummy/config/environment.js:66:    ENV.test.elasticsearch = process.env.FEDORA_ADAPTER_ES_SEARCH;
./tests/dummy/config/environment.js:70:    ENV.test.elasticsearch_index = process.env.FEDORA_ADAPTER_ES_INDEX;
./tests/integration/fedora-jsonld-test.js:26:  // Clear Fedora resources and Elasticsearch index for each test.
./tests/integration/fedora-jsonld-test.js:27:  // Small delays help indexer sync with Fedora and Elasticsearch
./tests/integration/fedora-jsonld-test.js:45:    let es_index = ENV.test.elasticsearch_index;
./tests/integration/fedora-jsonld-test.js:47:    return adapter.clearElasticsearch(es_index);
./README.md:7:This addon provides an adapter for interacting with the Fedora repository, http://fedorarepository.org/, and an Elasticsearch index of that data. The interaction is done through JSON-LD and the Fedora repository must have be modified in certain ways.
./README.md:15:* elasticsearchURI: Absolute URI to Elasticsearch search service.
./README.md:128:Store.query is implemented on top of Elasticsearch. Fedora must have been set up such
./README.md:129:that compacted Fedora objects are indexed in Elasticsearch. See https://github.com/OA-PASS/pass-indexer
./README.md:132:The query must be a clause in the Elasticsearch query syntax or an object containing that clause.
./README.md:133:See https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl.html. The clause
./README.md:153:Each property of a model object is available as an Elasticsearch field. The type of
./README.md:188:Docker containers which run Fedora, pass-indexer, and Elasticsearch must be configured in .env in order to run the integration tests.
./README.md:191:The file .esindex.config is used to create an Elasticsearch index for those objects.
./README.md:193:The Elasticsearch index will be available at http://localhost:9200/farm.
./.env:22:# Elasticsearch config
./.env:31:PI_ES_BASE=http://elasticsearch:9200/
./.env:32:PI_ES_INDEX=http://elasticsearch:9200/farm/
./docker-compose.yml:29:  elasticsearch:
./docker-compose.yml:30:    image: docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3
./docker-compose.yml:31:    container_name: elasticsearch
./docker-compose.yml:42:      - esdata:/usr/share/elasticsearch/data
./docker-compose.yml:43:      - ./.elasticsearch.yml:/usr/share/elasticsearch/config/elasticsearch.yml:Z
Binary file ./.git/index matches
./.wait.sh:3:# Wait until Fedora, Elasticsearch, and indexer are up
./.wait.sh:8:# Wait until Elasticsearch is up and indexer has created index
./.wait.sh:12:    echo "Waiting for response from Elasticsearch via ${CMD}"
./.wait.sh:34:    echo "Elasticsearch index is available"
