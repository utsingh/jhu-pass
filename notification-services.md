./notification-boot/src/test/resources/logback-test.xml:53:    <logger name="org.elasticsearch.client.RestClient" additivity="false" level="${org.elasticsearch.client.level:-ERROR}">
./notification-boot/src/test/resources/application.properties:28:pass.elasticsearch.url=http://${es.host:localhost}:${es.port:9200}/pass
./notification-boot/src/test/resources/application.properties:29:pass.elasticsearch.limit=100
./notification-boot/src/main/resources/logback.xml:52:    <logger name="org.elasticsearch.client.RestClient" additivity="false"
./notification-boot/src/main/resources/logback.xml:53:            level="${org.elasticsearch.client.level:-ERROR}">
./notification-boot/src/main/resources/application.properties:28:pass.elasticsearch.url=http://${es.host:localhost}:${es.port:9200}/pass
./notification-boot/src/main/resources/application.properties:29:pass.elasticsearch.limit=100
./notification-boot/src/main/java/org/dataconservancy/pass/notification/app/config/SpringBootNotificationConfig.java:84:    @Value("${pass.elasticsearch.url}")
./notification-boot/src/main/java/org/dataconservancy/pass/notification/app/config/SpringBootNotificationConfig.java:87:    @Value("${pass.elasticsearch.limit}")
./notification-boot/src/main/java/org/dataconservancy/pass/notification/app/config/SpringBootNotificationConfig.java:144:        if (!System.getProperties().containsKey("pass.elasticsearch.url")) {
./notification-boot/src/main/java/org/dataconservancy/pass/notification/app/config/SpringBootNotificationConfig.java:145:            System.setProperty("pass.elasticsearch.url", esUrl);
./notification-boot/src/main/java/org/dataconservancy/pass/notification/app/config/SpringBootNotificationConfig.java:148:        if (!System.getProperties().containsKey("pass.elasticsearch.limit")) {
./notification-boot/src/main/java/org/dataconservancy/pass/notification/app/config/SpringBootNotificationConfig.java:149:            System.setProperty("pass.elasticsearch.limit", String.valueOf(esLimit));
./pom.xml:192:        <docker.elasticsearch.version>docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3</docker.elasticsearch.version>
./pom.xml:210:        <pass.elasticsearch.host>${es.server}</pass.elasticsearch.host>
./pom.xml:211:        <pass.elasticsearch.url>http://${pass.elasticsearch.host}:${es.http.port}/pass/</pass.elasticsearch.url>
./pom.xml:212:        <pass.elasticsearch.limit>100</pass.elasticsearch.limit>
./pom.xml:291:                            <pass.elasticsearch.url>${pass.elasticsearch.url}</pass.elasticsearch.url>
./pom.xml:292:                            <pass.elasticsearch.limit>${pass.elasticsearch.limit}</pass.elasticsearch.limit>
./README.md:130:- `PASS_ELASTICSEARCH_URL` (`pass.elasticsearch.url`): `http://${es.host:localhost}:${es.port:9200}/pass`
./README.md:131:- `PASS_ELASTICSEARCH_LIMIT` (`pass.elasticsearch.limit`): `100`
./notification-integration/pom.xml:72:                                <argument>--pass.elasticsearch.url=${pass.elasticsearch.url}</argument>
./notification-integration/src/test/java/org/dataconservancy/pass/notification/NotificationSmokeIT.java:451:        assertTrue(System.getProperties().containsKey("pass.elasticsearch.url"));
./notification-integration/src/test/java/org/dataconservancy/pass/notification/NotificationSmokeIT.java:452:        assertTrue(System.getProperties().containsKey("pass.elasticsearch.limit"));
./dispatch-impl/src/test/java/logback-test.xml:46:    <logger name="org.elasticsearch.client.RestClient" additivity="false" level="${org.elasticsearch.client.level:-ERROR}">