./shared-assembler/src/test/resources/logback-test.xml:33:    <logger name="org.elasticsearch.client.RestClient" additivity="false" level="${org.elasticsearch.client.level:-ERROR}">
./deposit-integration/pom.xml:40:        <pass.elasticsearch.host>${docker.host.address}</pass.elasticsearch.host>
./deposit-integration/pom.xml:41:        <pass.elasticsearch.url>http://${pass.elasticsearch.host}:${es.port}/pass/</pass.elasticsearch.url>
./deposit-integration/pom.xml:405:                            <alias>elasticsearch</alias>
./deposit-integration/pom.xml:406:                            <name>${docker.elasticsearch.version}</name>
./deposit-integration/pom.xml:411:                                        <url>http://${pass.elasticsearch.host}:${es.port}/</url>
./deposit-integration/pom.xml:425:                                    <alias>elasticsearch</alias>
./deposit-integration/pom.xml:442:                                    <PI_ES_BASE>http://elasticsearch:9200/</PI_ES_BASE>
./deposit-integration/pom.xml:444:                                    <PI_ES_INDEX>http://elasticsearch:9200/pass/</PI_ES_INDEX>
./deposit-integration/pom.xml:506:                        <pass.elasticsearch.url>${pass.elasticsearch.url}</pass.elasticsearch.url>
./deposit-integration/src/test/resources/logback-test.xml:29:    <logger name="org.elasticsearch.client.RestClient" additivity="false" level="${org.elasticsearch.client.level:-ERROR}">
./deposit-integration/src/test/java/org/dataconservancy/pass/deposit/IndexSmokeIT.java:50:    private final String PASS_ES_URL = "pass.elasticsearch.url";
./shared-integration/src/test/resources/logback-test.xml:48:  <logger name="org.elasticsearch.client.RestClient" additivity="false" level="${org.elasticsearch.client.level:-ERROR}">
./shared-integration/src/test/java/org/dataconservancy/pass/deposit/integration/shared/SubmitAndValidatePackagesIT.java:206:     * The PASS Elastic Search URL (equivalent to the environment variable {@code PASS_ELASTICSEARCH_URL} or
./shared-integration/src/test/java/org/dataconservancy/pass/deposit/integration/shared/SubmitAndValidatePackagesIT.java:207:     * system property {@code pass.elasticsearch.url})
./shared-integration/src/test/java/org/dataconservancy/pass/deposit/integration/shared/SubmitAndValidatePackagesIT.java:255:     * the ElasticSearch index configuration.  {@code copyIndex()} attempts to copy an existing index to a new location
./shared-integration/src/test/java/org/dataconservancy/pass/deposit/integration/shared/SubmitAndValidatePackagesIT.java:271:        passIndexUrl = new URL(getenv().getOrDefault("PASS_ELASTICSEARCH_URL",
./shared-integration/src/test/java/org/dataconservancy/pass/deposit/integration/shared/SubmitAndValidatePackagesIT.java:272:                getProperty("pass.elasticsearch.url")));
./shared-integration/src/test/java/org/dataconservancy/pass/deposit/integration/shared/SubmitAndValidatePackagesIT.java:274:        assertNotNull("Missing value for PASS_ELASTICSEARCH_URL environment variable or " +
./shared-integration/src/test/java/org/dataconservancy/pass/deposit/integration/shared/SubmitAndValidatePackagesIT.java:275:                "pass.elasticsearch.url system property", passIndexUrl);
./shared-integration/src/test/java/org/dataconservancy/pass/deposit/integration/shared/SubmitAndValidatePackagesIT.java:598:     * Answers a {@code Function} that accepts the ElasticSearch index configuration, removes the {@code normalizer}
./shared-integration/src/test/java/org/dataconservancy/pass/deposit/integration/shared/SubmitAndValidatePackagesIT.java:626:     * Determines if the ElasticSearch configuration at the provided url carries a {@code normalizer} on the {@code
./shared-integration/src/test/java/org/dataconservancy/pass/deposit/integration/shared/SubmitAndValidatePackagesIT.java:630:     * @param passIndexUrl the URL to the ElasticSearch PASS index
./shared-integration/src/test/java/org/dataconservancy/pass/deposit/integration/shared/IndexUtil.java:220:     * Given a URL to an ElasticSearch index, determines the name of the index from the last path component.
./pom.xml:166:        <docker.elasticsearch.version>docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3</docker.elasticsearch.version>
./README.md:36:|`PASS_ELASTICSEARCH_LIMIT`                     |100                                                                            |the maximum number of results returned in a single search response
./README.md:37:|`PASS_ELASTICSEARCH_URL`                       |http://${es.host:localhost}:${es.port:9200}/pass                               |the URL used to communicate with the Elastic search API.  Normally this this variable does not need to be changed (see note below)
./README.md:48:> If the Elastic Search index is deployed under a url other than `/pass`, or if `https` ought to be used instead of `http`, the environment variable `PASS_ELASTICSEARCH_URL` must be set to the base of the Elastic Search HTTP API (e.g. `PASS_ELASTICSEARCH_URL=https://localhost:9200/index`)
./deposit-messaging/Dockerfile:13:ARG PASS_ELASTICSEARCH_URL
./deposit-messaging/Dockerfile:14:ARG PASS_ELASTICSEARCH_LIMIT
./deposit-messaging/Dockerfile:36:    ES_HOST=${ES_HOST:-elasticsearch} \
./deposit-messaging/Dockerfile:41:    PASS_ELASTICSEARCH_LIMIT=${PASS_ELASTICSEARCH_LIMIT:-100} \
./deposit-messaging/src/main/resources/logback.xml:90:  <logger name="org.elasticsearch.client.RestClient" additivity="false" level="${org.elasticsearch.client.level:-ERROR}">
./deposit-messaging/src/main/resources/application.properties:24:pass.elasticsearch.url=http://${es.host:localhost}:${es.port:9200}/pass
./deposit-messaging/src/main/resources/application.properties:25:pass.elasticsearch.limit=100
./deposit-messaging/src/main/java/org/dataconservancy/pass/deposit/messaging/config/spring/DepositConfig.java:97:    @Value("${pass.elasticsearch.url}")
./deposit-messaging/src/main/java/org/dataconservancy/pass/deposit/messaging/config/spring/DepositConfig.java:100:    @Value("${pass.elasticsearch.limit}")
./deposit-messaging/src/main/java/org/dataconservancy/pass/deposit/messaging/config/spring/DepositConfig.java:129:        if (!System.getProperties().containsKey("pass.elasticsearch.url")) {
./deposit-messaging/src/main/java/org/dataconservancy/pass/deposit/messaging/config/spring/DepositConfig.java:130:            System.setProperty("pass.elasticsearch.url", esUrl);
./deposit-messaging/src/main/java/org/dataconservancy/pass/deposit/messaging/config/spring/DepositConfig.java:133:        if (!System.getProperties().containsKey("pass.elasticsearch.limit")) {
./deposit-messaging/src/main/java/org/dataconservancy/pass/deposit/messaging/config/spring/DepositConfig.java:134:            System.setProperty("pass.elasticsearch.limit", String.valueOf(esLimit));
./deposit-messaging/src/main/java/org/dataconservancy/pass/deposit/messaging/service/SubmissionStatusUpdater.java:44: * the ElasticSearch DSL, and communicate directly with the ElasticSearch Query API.  This allows more surgical
