./pass-indexer-cli/src/main/java/org/dataconservancy/pass/indexer/Main.java:46:            serv.setElasticsearchIndexUrl(get_config("PI_ES_INDEX"));
./pass-indexer-cli/src/main/java/org/dataconservancy/pass/indexer/Main.java:47:            serv.setElasticsearchIndexConfig(get_config("PI_ES_CONFIG", null));            
./README.md:6:The pass-indexer keeps an [Elasticsearch](https://github.com/elastic/elasticsearch) index up to date with resources in a
./README.md:14:The Elasticsearch index is created on startup if it does not exist with a set [configuration](pass-indexer-core/src/main/resources/esindex.json).
./README.md:17:The Elasticsearch document is the compact JSON-LD representation of that resource without server triples. If a key on the document is not present
./README.md:20:When there is a message about a resource of a type being monitored, the indexer either creates a corresponding document in Elasticsearch 
./README.md:22:configured prefix, PI_TYPE_PREFIX, are handled. The id of the Elasticsearch document is the safe URL base64 encoding of resource path. This lets both the document be created and updated with the same PUT.
./README.md:31:A consequence of the auto-completion is that NAME_suggest fields will appear in the _source document returned by Elasticsearch.
./README.md:32:See https://www.elastic.co/guide/en/elasticsearch/reference/current/search-request-source-filtering.html for options.
./README.md:76:* PI_ES_INDEX=http://elasticsearch:9200/pass/
./.env:20:# Elasticsearch config
./docker-compose.yml:17:  elasticsearch:
./docker-compose.yml:18:    image: docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3
./docker-compose.yml:19:    container_name: elasticsearch
./docker-compose.yml:30:      - esdata:/usr/share/elasticsearch/data
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/PassIndexerIT.java:48:		serv.setElasticsearchIndexUrl("http://localhost:9200/pass/");
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/PassIndexerIT.java:49:		serv.setElasticsearchIndexConfig("/esindex.json");
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/PassIndexerIT.java:108:	// Execute an Elasticsearch query and return the result
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/PassIndexerIT.java:187:			assertTrue("No Elasticsearch document: " + uri, false);
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/PassIndexerIT.java:200:	// Check that Elasticsearch document is created for a Fedora User resource.
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/ElasticSearchIndexerTest.java:26:public class ElasticSearchIndexerTest implements IndexerConstants {
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/ElasticSearchIndexerTest.java:28:    private ElasticSearchIndexer indexer;
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/ElasticSearchIndexerTest.java:38:        // GET for Elasticsearch index
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/ElasticSearchIndexerTest.java:41:        // GET for Elasticsearch index config. Use URL for config to test support.
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/ElasticSearchIndexerTest.java:42:        try (InputStream is = ElasticSearchIndexerTest.class.getResourceAsStream("/esindex.json")) {
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/ElasticSearchIndexerTest.java:47:        // PUT to create Elasticsearch index
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/ElasticSearchIndexerTest.java:50:        indexer = new ElasticSearchIndexer(es_index_url.toString(), es_config_url.toString(), "admin", "admin");
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/ElasticSearchIndexerTest.java:82:        // POST to Elasticsearch
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/ElasticSearchIndexerTest.java:107:        // Check the JSON posted to Elasticsearch. 
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/ElasticSearchIndexerTest.java:114:        // Should have projectName_suggest added for projectName by Elasticsearch 
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/ElasticSearchIndexerTest.java:174:        // POST to Elasticsearch
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/ElasticSearchIndexerTest.java:210:        // DELETE to Elasticsearch
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/FedoraIndexerServiceTest.java:33:        // GET for Elasticsearch index config
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/FedoraIndexerServiceTest.java:36:        // PUT for Elasticsearch index config
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/FedoraIndexerServiceTest.java:43:        service.setElasticsearchIndexUrl(es_index_url.toString());
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/FedoraIndexerServiceTest.java:44:        service.setElasticsearchIndexConfig("/esindex.json");
./pass-indexer-core/src/test/java/org/dataconservancy/pass/indexer/FedoraIndexerServiceTest.java:81:        // POST to Elasticsearch
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/FedoraIndexerService.java:14: * Elasticsearch index in response.
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/FedoraIndexerService.java:23:    private String elasticsearch_index_url;
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/FedoraIndexerService.java:26:    private String elasticsearch_index_config;
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/FedoraIndexerService.java:40:    public void setElasticsearchIndexUrl(String elasticsearch_index_url) {
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/FedoraIndexerService.java:41:        this.elasticsearch_index_url = elasticsearch_index_url;
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/FedoraIndexerService.java:44:    public void setElasticsearchIndexConfig(String elasticsearch_index_config) {
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/FedoraIndexerService.java:45:        this.elasticsearch_index_config = elasticsearch_index_config;
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/FedoraIndexerService.java:67:        if (elasticsearch_index_url == null) {
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/FedoraIndexerService.java:73:        if (elasticsearch_index_config == null) {
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/FedoraIndexerService.java:81:        ElasticSearchIndexer es = new ElasticSearchIndexer(elasticsearch_index_url, elasticsearch_index_config, fedora_user, fedora_pass);
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/FedoraIndexerService.java:100:        LOG.info("Elasticsearch index: " + elasticsearch_index_url);
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/ElasticSearchIndexer.java:32: * The compact JSON-LD representation must be simple enough for Elasticsearch to understand.
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/ElasticSearchIndexer.java:44:public class ElasticSearchIndexer implements IndexerConstants {
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/ElasticSearchIndexer.java:46:    private static final Logger LOG = LoggerFactory.getLogger(ElasticSearchIndexer.class);
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/ElasticSearchIndexer.java:58:     * If the given Elasticsearch index does not exist, create it using the supplied configuration.
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/ElasticSearchIndexer.java:67:    public ElasticSearchIndexer(String es_index_url, String es_index_config, String fedora_user, String fedora_pass) throws IOException {
./pass-indexer-core/src/main/java/org/dataconservancy/pass/indexer/ElasticSearchIndexer.java:272:    // Create or update the document corresponding to a Fedora resource in Elasticsearch.
Binary file ./.git/objects/pack/pack-ee41f0704caf701b476aa2a00964ee4c84588ede.pack matches
Binary file ./.git/index matches
./.wait.sh:35:    echo "Waiting for response from Elasticsearch via ${CMD}"
./.wait.sh:57:    echo "Elasticsearch is up"
