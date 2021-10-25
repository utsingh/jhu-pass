# Java Fedora Client

## upgrade elasticsearch 7 in java fedora client
grep -inr "docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3" .
./pom.xml:130:              <name>docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3</name>

--> Change this to "docker.elastic.co/elasticsearch/elasticsearch:7.15.1"

## grep -inr "elasticsearch" .

### POM.xml declarations
*Maven Project Object Model (POM) file in XML format for delcaring project information.*

./pass-data-client/pom.xml:43:      <groupId>org.elasticsearch.client</groupId>
./pass-data-client/pom.xml:44:      <artifactId>elasticsearch-rest-high-level-client</artifactId>

./pom.xml:134:    <elasticsearch-client.version>6.7.2</elasticsearch-client.version>
./pom.xml:325:        <groupId>org.elasticsearch.client</groupId>
./pom.xml:326:        <artifactId>elasticsearch-rest-high-level-client</artifactId>
./pom.xml:327:        <version>${elasticsearch-client.version}</version>


### Pass Data Client
*Creates instances of objects needed to perform PassClient requirements, and redirects to appropriate service (Index client or CRUD client).*

1. PassClientDefault.java: public class PassClientDefault implements 

ES Variable: indexClient = new ElasticsearchPassClient();

- findByAttribute: takes in modelClass, sttribute, and value.
- findAllByAttribute: takes in modelClass, sttribute, and value.
- overloaded findAllByAttribute: takes in modelClass, attribute, value, limit, offset.
- multi-sttributes findAllByAttributes: takes in modelClass, valueAttributesMap.
- overloaded findAllByAttributes: takes in modelClass, valueAttributesMap, limit, offset.

./pass-data-client/src/main/java/org/dataconservancy/pass/client/PassClientDefault.java:28:import org.dataconservancy.pass.client.elasticsearch.ElasticsearchPassClient;
./pass-data-client/src/main/java/org/dataconservancy/pass/client/PassClientDefault.java:47:    private ElasticsearchPassClient indexClient;
./pass-data-client/src/main/java/org/dataconservancy/pass/client/PassClientDefault.java:54:        indexClient = new ElasticsearchPassClient();

2. elasticsearch/ElasticsearchPassClient.java

URL(s) of indexer: private final HttpHost[] hosts;
Names of indexes: private final String[] indices;

Retrieve Search Results from ElasticSearch: getIndexerResults(String querystring, int limit, int offset)
Search the index using querystring: {}, with limit {} and offset {}", querystring,  limit, offset)


./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:16:package org.dataconservancy.pass.client.elasticsearch;
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:37:import org.elasticsearch.action.search.SearchRequest;
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:38:import org.elasticsearch.action.search.SearchResponse;
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:39:import org.elasticsearch.client.RestClient;
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:40:import org.elasticsearch.client.RestHighLevelClient;
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:41:import org.elasticsearch.index.query.Operator;
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:42:import org.elasticsearch.index.query.QueryStringQueryBuilder;
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:43:import org.elasticsearch.search.SearchHit;
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:44:import org.elasticsearch.search.SearchHits;
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:45:import org.elasticsearch.search.builder.SearchSourceBuilder;
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:50: * Communicates with elasticsearch
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:53:public class ElasticsearchPassClient {
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:56:    private static final Logger LOG = LoggerFactory.getLogger(ElasticsearchPassClient.class);
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:90:    public ElasticsearchPassClient() {
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:91:        Set<URL> indexerUrls = ElasticsearchConfig.getIndexerHostUrl();      
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:99:        indices = ElasticsearchConfig.getIndices();
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:155:        return findAllByAttribute(modelClass, attribute, value, ElasticsearchConfig.getIndexerLimit(), 0);
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:203:        return findAllByAttributes(modelClass, valueAttributesMap, ElasticsearchConfig.getIndexerLimit(), 0);
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:246:     * Retrieve search results from elasticsearch

3. elasticsearch/ElasticsearchConfig.java
*config file*

./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchConfig.java:16:package org.dataconservancy.pass.client.elasticsearch;
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchConfig.java:32:public class ElasticsearchConfig {
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchConfig.java:34:    private static final Logger LOG = LoggerFactory.getLogger(ElasticsearchConfig.class);
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchConfig.java:36:    private static final String INDEXER_URL_KEY = "pass.elasticsearch.url";
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchConfig.java:39:    private static final String INDICES_KEY = "pass.elasticsearch.indices";
./pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchConfig.java:42:    private static final String INDEXER_LIMIT_KEY = "pass.elasticsearch.limit";

### PASS Client API
* Takes any PassEntity and persists it in the database, returns the URI if successful or appropriate exception if not. Note that PassEntities that are being created should have null as their ID, the URI will the the ID field when reading the resource back.
* Takes modelObj The entity to be created
* returns URI of new record

Implements the following ES methods:
- createResource(PassEntity modelObj)
- createAndReadResource(T modelObj, Class<T> modelClass)
- updateResource(PassEntity modelObj)
- updateAndReadResource(T modelObj, Class<T> modelClass)
- deleteResource(URI uri)
- readResource(URI uri, Class<T> modelClass)

- findByAttribute(Class<T> modelClass, String attribute, Object value)
- findAllByAttribute(Class<T> modelClass, String attribute, Object value)
- findAllByAttribute(Class<T> modelClass, String attribute, Object value, int limit, int offset)
- findAllByAttribute(Class<T> modelClass, String attribute, Object value, int limit, int offset)
- findAllByAttributes(Class<T> modelClass, Map<String, Object> attributeValuesMap, int limit, int offset)
- getIncoming(URI passEntity)
- upload(URI entityUri, InputStream content)
- upload(URI entityUri, InputStream content, Map<String, ?> params)
- processAllEntities(Consumer<URI> processor, Class<T> modelClass)

./pass-client-api/src/main/java/org/dataconservancy/pass/client/PassClient.java:135:     * By default this will return a maximum of 200 matching records, unless the pass.elasticsearch.limit
./pass-client-api/src/main/java/org/dataconservancy/pass/client/PassClient.java:201:     * By default this will return a maximum of 200 matching records, unless the pass.elasticsearch.limit

### PASS Client Integration
* CLient Integration POM file

./pass-client-integration/pom.xml:106:                  <PI_ES_BASE>http://elasticsearch:9200/</PI_ES_BASE>
./pass-client-integration/pom.xml:107:                  <PI_ES_INDEX>http://elasticsearch:9200/pass/</PI_ES_INDEX>
./pass-client-integration/pom.xml:115:                  <link>elasticsearch</link>
./pass-client-integration/pom.xml:129:              <alias>elasticsearch</alias>
./pass-client-integration/pom.xml:130:              <name>docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3</name>
./pass-client-integration/pom.xml:144:                  <alias>elasticsearch</alias>
./pass-client-integration/pom.xml:181:            <pass.elasticsearch.url>http://${ES_HOST}:${ES_PORT}</pass.elasticsearch.url>

* Base client for client ITs.
./pass-client-integration/src/test/java/org/dataconservancy/pass/client/integration/ClientITBase.java:86:        if (System.getProperty("pass.elasticsearch.url") == null) {
./pass-client-integration/src/test/java/org/dataconservancy/pass/client/integration/ClientITBase.java:87:            System.setProperty("pass.elasticsearch.url", "http://localhost:9200/pass/");

### Miscelleneous
./README.md:12:The interfaces in `pass-client-api` can be used to access both Fedora and Elasticsearch
./README.md:88:* pass.elasticsearch.url (defaults = http://localhost:9200)
./README.md:89:* pass.elasticsearch.indices (default = pass)
./README.md:90:* pass.elasticsearch.limit (defaults = 200) you can also override the default by using the findBy functions that accept a limit and offset value

./README.md:92:A note on pass.elasticsearch.indices: a value of "" will cause all indices on the host to be searched, as should a target value of _all or *.

./README.md:94:## Integration tests with Fedora and Elasticsearch
./README.md:96:The integration test module `pass-client-integration` uses Docker to spin up an instance of Fedora and Elasticsearch for testing the client against.

./README.md:102:This will run Fedora at standard port (8080) and Elasticsearch at port 9200. This mode is very useful for testing/debugging/developing against the databases from within the IDE.   Repository content is stored in `target`, so if it is run after integration tests, the repository will still retain all data deposited during.

Binary file ./.git/index matches

./.travis.yml:34:  - docker logs elasticsearch


# pass-ember


