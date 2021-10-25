./provider-integration/pom.xml:39:        <pass.elasticsearch.host>${docker.host.address}</pass.elasticsearch.host>
./provider-integration/pom.xml:40:        <pass.elasticsearch.url>http://${pass.elasticsearch.host}:${es.port}/pass/</pass.elasticsearch.url>
./provider-integration/pom.xml:41:        <pass.elasticsearch.limit>100</pass.elasticsearch.limit>
./provider-integration/pom.xml:242:                                    <alias>elasticsearch</alias>
./provider-integration/pom.xml:243:                                    <name>${docker.elasticsearch.version}</name>
./provider-integration/pom.xml:248:                                                <url>http://${pass.elasticsearch.host}:${es.port}/</url>
./provider-integration/pom.xml:262:                                            <alias>elasticsearch</alias>
./provider-integration/pom.xml:275:                                            <PI_ES_BASE>http://elasticsearch:9200/</PI_ES_BASE>
./provider-integration/pom.xml:276:                                            <PI_ES_INDEX>http://elasticsearch:9200/pass/</PI_ES_INDEX>
./provider-integration/pom.xml:337:                        <pass.elasticsearch.url>${pass.elasticsearch.url}</pass.elasticsearch.url>
./provider-integration/pom.xml:338:                        <pass.elasticsearch.limit>${pass.elasticsearch.limit}</pass.elasticsearch.limit>
./provider-integration/src/test/resources/logback-test.xml:52:    <!-- org.dataconservancy.pass.client.elasticsearch.ElasticsearchPassClient -->
./provider-integration/src/test/resources/logback-test.xml:53:    <logger name="org.dataconservancy.pass.client.elasticsearch.ElasticsearchPassClient" additivity="false"
./provider-integration/src/test/resources/logback-test.xml:58:    <logger name="org.elasticsearch.client.RestClient" additivity="false"
./provider-integration/src/test/resources/logback-test.xml:59:            level="${org.elasticsearch.client.level:-ERROR}">
./provider-integration/src/test/java/edu/jhu/library/pass/deposit/provider/integration/SpringContextConfiguration.java:38:    @Value("${pass.elasticsearch.url}")
./provider-integration/src/test/java/edu/jhu/library/pass/deposit/provider/integration/SpringContextConfiguration.java:41:    @Value("${pass.elasticsearch.limit}")
./provider-integration/src/test/java/edu/jhu/library/pass/deposit/provider/integration/SpringContextConfiguration.java:67:        if (!System.getProperties().containsKey("pass.elasticsearch.url")) {
./provider-integration/src/test/java/edu/jhu/library/pass/deposit/provider/integration/SpringContextConfiguration.java:68:            System.setProperty("pass.elasticsearch.url", esUrl);
./provider-integration/src/test/java/edu/jhu/library/pass/deposit/provider/integration/SpringContextConfiguration.java:71:        if (!System.getProperties().containsKey("pass.elasticsearch.limit")) {
./provider-integration/src/test/java/edu/jhu/library/pass/deposit/provider/integration/SpringContextConfiguration.java:72:            System.setProperty("pass.elasticsearch.limit", String.valueOf(esLimit));
./pom.xml:159:        <docker.elasticsearch.version>docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3</docker.elasticsearch.version>
./bagit-package-provider/pom.xml:133:                    <!-- org.elasticsearch.client:elasticsearch-rest-high-level-client -->
./bagit-package-provider/pom.xml:134:                    <groupId>org.elasticsearch.client</groupId>
./bagit-package-provider/pom.xml:135:                    <artifactId>elasticsearch-rest-high-level-client</artifactId>
