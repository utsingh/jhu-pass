./.docker/.harvard_env:53:PASS_ELASTICSEARCH_URL=http://elasticsearch:9200
./.docker/.harvard_env:69:# Elasticsearch config
./.docker/.harvard_env:78:PI_ES_BASE=http://elasticsearch:9200/
./.docker/.harvard_env:79:PI_ES_INDEX=http://elasticsearch:9200/pass/
./.docker/.env:44:PASS_ELASTICSEARCH_URL=http://elasticsearch:9200
./.docker/.env:48:# Elasticsearch config
./.docker/.env:57:PI_ES_BASE=http://elasticsearch:9200/
./.docker/.env:58:PI_ES_INDEX=http://elasticsearch:9200/pass/
./.docker/docker-compose.yml:117:  elasticsearch:
./.docker/docker-compose.yml:118:    #image: docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3@sha256:ccfad77c0731c010e6ff8c43b4ab50f5ce90c0fa4e65846530779c5c6707c20a
./.docker/docker-compose.yml:119:    image: docker.elastic.co/elasticsearch/elasticsearch:7.15.1
./.docker/docker-compose.yml:120:    container_name: elasticsearch
./.docker/docker-compose.yml:131:      - passdata:/usr/share/elasticsearch/data
./.docker/harvard.yml:107:  elasticsearch:
./.docker/harvard.yml:108:    image: docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3@sha256:ccfad77c0731c010e6ff8c43b4ab50f5ce90c0fa4e65846530779c5c6707c20a
./.docker/harvard.yml:109:    container_name: elasticsearch
./.docker/harvard.yml:120:      - passdata-harvard:/usr/share/elasticsearch/data
./app/adapters/application.js:9:  elasticsearchURI = ENV.fedora.elasticsearch;
./app/routes/dashboard.js:22:    let approvalResults = await this.ajax.post(ENV.fedora.elasticsearch, {
./app/routes/dashboard.js:38:    let editsResults = await this.ajax.post(ENV.fedora.elasticsearch, {
./app/services/search-helper.js:6: * This service can be referenced by components that rely on Elasticsearch query results
./app/services/search-helper.js:74:   * Wait for Elasticsearch to be reindexed with the given value.
./app/services/autocomplete.js:6: * Service designed to hit the Elasticsearch autocomplete service to get suggestions
./app/services/autocomplete.js:23:    return ENV.fedora.elasticsearch;
./app/services/autocomplete.js:112:   * Adapt Elasticsearch results to a flat array.
./app/services/autocomplete.js:115:   * 'response.suggest' is where Elasticsearch sticks the autocomplete suggestions.
./app/services/autocomplete.js:122:   * @param {object} response response from Elasticsearch
./dist/index.html:10:<meta name="pass-ember/config/environment" content="%7B%22modulePrefix%22%3A%22pass-ember%22%2C%22environment%22%3A%22development%22%2C%22rootURL%22%3A%22%2Fapp%2F%22%2C%22host%22%3A%22http%3A%2F%2Flocalhost%3A8080%22%2C%22locationType%22%3A%22auto%22%2C%22ember-load%22%3A%7B%22loadingIndicatorClass%22%3A%22app-loader%22%7D%2C%22EmberENV%22%3A%7B%22FEATURES%22%3A%7B%7D%2C%22EXTEND_PROTOTYPES%22%3A%7B%22Date%22%3Afalse%7D%2C%22_APPLICATION_TEMPLATE_WRAPPER%22%3Afalse%2C%22_DEFAULT_ASYNC_OBSERVERS%22%3Atrue%2C%22_JQUERY_INTEGRATION%22%3Atrue%2C%22_TEMPLATE_ONLY_GLIMMER_COMPONENTS%22%3Atrue%7D%2C%22APP%22%3A%7B%22staticConfigUri%22%3A%22%2Fconfig.json%22%2C%22name%22%3A%22pass-ember%22%2C%22version%22%3A%220.0.4%2Ba5f43647%22%7D%2C%22ember-cli-mirage%22%3A%7B%22enabled%22%3Afalse%2C%22usingProxy%22%3Afalse%2C%22useDefaultPassthroughs%22%3Atrue%7D%2C%22fedora%22%3A%7B%22base%22%3A%22https%3A%2F%2Fpass.local%2Ffcrepo%2Frest%2F%22%2C%22context%22%3A%22https%3A%2F%2Foa-pass.github.io%2Fpass-data-model%2Fsrc%2Fmain%2Fresources%2Fcontext-3.5.jsonld%22%2C%22data%22%3A%22http%3A%2F%2Foapass.org%2Fns%2Fpass%23%22%2C%22elasticsearch%22%3A%22https%3A%2F%2Fpass.local%2Fes%2F%22%2C%22username%22%3A%22admin%22%2C%22password%22%3A%22moo%22%7D%2C%22userService%22%3A%7B%22url%22%3A%22https%3A%2F%2Fpass.local%2Fpass-user-service%2Fwhoami%22%7D%2C%22doiService%22%3A%7B%22url%22%3A%22https%3A%2F%2Fpass.local%2Fdoiservice%2Fjournal%22%7D%2C%22schemaService%22%3A%7B%22url%22%3A%22https%3A%2F%2Fpass.local%2Fschemaservice%22%7D%2C%22policyService%22%3A%7B%22url%22%3A%22https%3A%2F%2Fpass.local%2Fpolicyservice%22%2C%22policySuffix%22%3A%22%2Fpolicies%22%2C%22repoSuffix%22%3A%22%2Frepositories%22%7D%2C%22oaManuscriptService%22%3A%7B%22lookupUrl%22%3A%22%2Fdownloadservice%2Flookup%22%2C%22downloadUrl%22%3A%22%2Fdownloadservice%2Fdownload%22%7D%2C%22metadataSchemaUri%22%3A%22https%3A%2F%2Foa-pass.github.io%2Fmetadata-schemas%2Fjhu%2Fglobal.json%22%2C%22exportApplicationGlobal%22%3Atrue%2C%22ember-modal-dialog%22%3A%7B%22hasEmberTether%22%3A%221.0.0%22%7D%2C%22ember-a11y-testing%22%3A%7B%22componentOptions%22%3A%7B%22axeOptions%22%3A%7B%22rules%22%3A%7B%7D%7D%7D%7D%7D" />
./dist/tests/index.html:11:<meta name="pass-ember/config/environment" content="%7B%22modulePrefix%22%3A%22pass-ember%22%2C%22environment%22%3A%22test%22%2C%22rootURL%22%3A%22%2Fapp%2F%22%2C%22host%22%3A%22http%3A%2F%2Flocalhost%3A8080%22%2C%22locationType%22%3A%22none%22%2C%22ember-load%22%3A%7B%22loadingIndicatorClass%22%3A%22app-loader%22%7D%2C%22EmberENV%22%3A%7B%22FEATURES%22%3A%7B%7D%2C%22EXTEND_PROTOTYPES%22%3A%7B%22Date%22%3Afalse%7D%2C%22_APPLICATION_TEMPLATE_WRAPPER%22%3Afalse%2C%22_DEFAULT_ASYNC_OBSERVERS%22%3Atrue%2C%22_JQUERY_INTEGRATION%22%3Atrue%2C%22_TEMPLATE_ONLY_GLIMMER_COMPONENTS%22%3Atrue%7D%2C%22APP%22%3A%7B%22staticConfigUri%22%3A%22%2Fconfig.json%22%2C%22autoboot%22%3Afalse%2C%22LOG_ACTIVE_GENERATION%22%3Afalse%2C%22LOG_VIEW_LOOKUPS%22%3Afalse%2C%22rootElement%22%3A%22%23ember-testing%22%2C%22name%22%3A%22pass-ember%22%2C%22version%22%3A%220.0.4%2Ba5f43647%22%7D%2C%22ember-cli-mirage%22%3A%7B%22enabled%22%3Atrue%2C%22usingProxy%22%3Afalse%2C%22useDefaultPassthroughs%22%3Atrue%7D%2C%22fedora%22%3A%7B%22base%22%3A%22https%3A%2F%2Fpass.local%2Ffcrepo%2Frest%2F%22%2C%22context%22%3A%22https%3A%2F%2Foa-pass.github.io%2Fpass-data-model%2Fsrc%2Fmain%2Fresources%2Fcontext-3.5.jsonld%22%2C%22data%22%3A%22http%3A%2F%2Foapass.org%2Fns%2Fpass%23%22%2C%22elasticsearch%22%3A%22https%3A%2F%2Fpass.local%2Fes%2F%22%2C%22username%22%3A%22admin%22%2C%22password%22%3A%22moo%22%7D%2C%22userService%22%3A%7B%22url%22%3A%22https%3A%2F%2Fpass.local%2Fpass-user-service%2Fwhoami%22%7D%2C%22doiService%22%3A%7B%22url%22%3A%22https%3A%2F%2Fpass.local%2Fdoiservice%2Fjournal%22%7D%2C%22schemaService%22%3A%7B%22url%22%3A%22https%3A%2F%2Fpass.local%2Fschemaservice%22%7D%2C%22policyService%22%3A%7B%22url%22%3A%22https%3A%2F%2Fpass.local%2Fpolicyservice%22%2C%22policySuffix%22%3A%22%2Fpolicies%22%2C%22repoSuffix%22%3A%22%2Frepositories%22%7D%2C%22oaManuscriptService%22%3A%7B%22lookupUrl%22%3A%22%2Fdownloadservice%2Flookup%22%2C%22downloadUrl%22%3A%22%2Fdownloadservice%2Fdownload%22%7D%2C%22metadataSchemaUri%22%3A%22https%3A%2F%2Foa-pass.github.io%2Fmetadata-schemas%2Fjhu%2Fglobal.json%22%2C%22exportApplicationGlobal%22%3Atrue%2C%22ember-modal-dialog%22%3A%7B%22hasEmberTether%22%3A%221.0.0%22%7D%2C%22ember-a11y-testing%22%3A%7B%22componentOptions%22%3A%7B%22axeOptions%22%3A%7B%22rules%22%3A%7B%7D%7D%7D%7D%7D" />
./dist/assets/pass-ember.js:33:      (0, _defineProperty2.default)((0, _assertThisInitialized2.default)(_this), "elasticsearchURI", _environment.default.fedora.elasticsearch);
./dist/assets/pass-ember.js:62:  //   elasticsearchURI: Absolute URI of Elasticsearch search service.
./dist/assets/pass-ember.js:130:    // Return a Promise which clears the specified Elasticsearch index
./dist/assets/pass-ember.js:131:    clearElasticsearch: function clearElasticsearch(index_url) {
./dist/assets/pass-ember.js:239:      which performs poorly, use Elasticsearch and return up to 100.
./dist/assets/pass-ember.js:256:    // Create an elasticsearch query that restricts the given query to the given type.
./dist/assets/pass-ember.js:258:    _create_elasticsearch_query: function _create_elasticsearch_query(query, jsonld_type) {
./dist/assets/pass-ember.js:287:    // Turn Elasticsearch results into a JSON-LD @graph suitable for normalizeResponse.
./dist/assets/pass-ember.js:289:    _parse_elasticsearch_result: function _parse_elasticsearch_result(result, info) {
./dist/assets/pass-ember.js:303:       Elasticsearch query.
./dist/assets/pass-ember.js:304:        The query must be a clause in the Elasticsearch query syntax or an object
./dist/assets/pass-ember.js:306:       See https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl.html.
./dist/assets/pass-ember.js:322:        Each property of a model object is available as an Elasticsearch field. The type of
./dist/assets/pass-ember.js:334:      var url = this.get('elasticsearchURI');
./dist/assets/pass-ember.js:343:      var data = this._create_elasticsearch_query(_query, jsonld_type);
./dist/assets/pass-ember.js:353:        return _this3._parse_elasticsearch_result(result, info);
./dist/assets/pass-ember.js:12908:;define("pass-ember/mirage/config", ["exports", "pass-ember/config/environment", "pass-ember/mirage/routes/users", "pass-ember/mirage/routes/elastic-search", "pass-ember/mirage/routes/journals", "pass-ember/mirage/routes/policies", "pass-ember/mirage/routes/funders", "pass-ember/mirage/routes/repositories", "pass-ember/mirage/routes/publications", "pass-ember/mirage/routes/submissions", "pass-ember/mirage/routes/submission-events", "pass-ember/mirage/routes/files", "pass-ember/mirage/routes/schemas", "pass-ember/mirage/routes/grants"], function (_exports, _environment, _users, _elasticSearch, _journals, _policies, _funders, _repositories, _publications, _submissions, _submissionEvents, _files, _schemas, _grants) {
./dist/assets/pass-ember.js:12919:    (0, _elasticSearch.default)(this);
./dist/assets/pass-ember.js:17833:                  return this.ajax.post(_environment.default.fedora.elasticsearch, {
./dist/assets/pass-ember.js:17869:                  return this.ajax.post(_environment.default.fedora.elasticsearch, {
./dist/assets/pass-ember.js:19717:   * Service designed to hit the Elasticsearch autocomplete service to get suggestions
./dist/assets/pass-ember.js:19849:       * Adapt Elasticsearch results to a flat array.
./dist/assets/pass-ember.js:19852:       * 'response.suggest' is where Elasticsearch sticks the autocomplete suggestions.
./dist/assets/pass-ember.js:19859:       * @param {object} response response from Elasticsearch
./dist/assets/pass-ember.js:19908:        return _environment.default.fedora.elasticsearch;
./dist/assets/pass-ember.js:21343:   * This service can be referenced by components that rely on Elasticsearch query results
./dist/assets/pass-ember.js:21426:       * Wait for Elasticsearch to be reindexed with the given value.
./config/environment.js:66:    elasticsearch: 'http://localhost:9200/pass/_search'
./config/environment.js:128:    ENV.fedora.elasticsearch = process.env.FEDORA_ADAPTER_ES;
./README.md:10:Objects persisted to Fedora are automatically indexed by Elasticsearch. See
./README.md:12:Note that the indexing process is asynchronous. An object persisted to Fedora will not immediately be available in Elasticsearch.
./README.md:53:* Elasticsearch index search endpoint is at https://pass.local/es/
./README.md:68:and Elasticsearch are and generally will not need to be modified during development.
./README.md:70:In order to prevent an Authorization header being sent to Fedora and Elasticsearch,