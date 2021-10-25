./pom.xml:72:        <docker.elasticsearch.version>docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3</docker.elasticsearch.version>
./pom.xml:86:        <pass.elasticsearch.host>${docker.host.address}</pass.elasticsearch.host>
./pom.xml:87:        <pass.elasticsearch.url>http://${pass.elasticsearch.host}:${es.port}/pass/</pass.elasticsearch.url>
./pom.xml:88:        <pass.elasticsearch.limit>100</pass.elasticsearch.limit>
./pom.xml:240:                                    <alias>elasticsearch</alias>
./pom.xml:241:                                    <name>${docker.elasticsearch.version}</name>
./pom.xml:246:                                                <url>http://${pass.elasticsearch.host}:${es.port}/</url>
./pom.xml:260:                                            <alias>elasticsearch</alias>
./pom.xml:273:                                            <PI_ES_BASE>http://elasticsearch:9200/</PI_ES_BASE>
./pom.xml:274:                                            <PI_ES_INDEX>http://elasticsearch:9200/pass/</PI_ES_INDEX>
./pom.xml:314:                        <pass.elasticsearch.url>${pass.elasticsearch.url}</pass.elasticsearch.url>
./pom.xml:315:                        <pass.elasticsearch.limit>${pass.elasticsearch.limit}</pass.elasticsearch.limit>
./Dockerfile-ITs:7:PASS_ELASTICSEARCH_URL=http://elasticsearch:9200/pass/ \
./Dockerfile-ITs:8:PASS_ELASTICSEARCH_LIMIT=${pass.elasticsearch.limit}
./README.md:29:PASS_ELASTICSEARCH_URL
./README.md:30:PASS_ELASTICSEARCH_LIMIT
./src/test/resources/logback-test.xml:44:    <!-- org.dataconservancy.pass.client.elasticsearch.ElasticsearchPassClient -->
./src/test/resources/logback-test.xml:45:    <logger name="org.dataconservancy.pass.client.elasticsearch.ElasticsearchPassClient" additivity="false"
./src/test/resources/logback-test.xml:50:    <logger name="org.elasticsearch.client.RestClient" additivity="false"
./src/test/resources/logback-test.xml:51:            level="${org.elasticsearch.client.level:-ERROR}">
