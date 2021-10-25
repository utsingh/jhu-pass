./pom.xml:80:    <elasticsearch.version>6.2.4</elasticsearch.version>
./pom.xml:364:        <groupId>org.elasticsearch.client</groupId>
./pom.xml:365:        <artifactId>elasticsearch-rest-high-level-client</artifactId>
./pom.xml:366:        <version>${elasticsearch.version}</version>
./README.md:19:* `PASS_ELASTICSEARCH_URL` (URI, default `http://localhost:9200/pass`).  The elasticsearch base URI
./README.md:27:* Standard pass client environment variables (`PASS_FEDORA_*`, `PASS_ELASTICSEARCH_*`).
./README.md:123:* Standard pass client environment variables (`PASS_FEDORA_*`, `PASS_ELASTICSEARCH_*`).
./pass-authz-core/pom.xml:27:                  <shadedPattern>org.dataconservancy.pass.auth.filters.shaded.org.elasticsearch</shadedPattern>
./pass-authz-core/pom.xml:28:                  <pattern>org.elasticsearch</pattern>
./.git/packed-refs:11:366001da69b3c97dfa643faf7069665c8ad45300 refs/remotes/origin/dependabot/maven/org.elasticsearch.client-elasticsearch-rest-high-level-client-7.13.4
./pass-authz-integration/pom.xml:132:            <pass.elasticsearch.url>http://${ES_HOST}:${ES_PORT}</pass.elasticsearch.url>
./pass-authz-integration/pom.xml:181:                  <PI_ES_BASE>http://elasticsearch:9200/</PI_ES_BASE>
./pass-authz-integration/pom.xml:182:                  <PI_ES_INDEX>http://elasticsearch:9200/pass/</PI_ES_INDEX>
./pass-authz-integration/pom.xml:192:                  <link>elasticsearch</link>
./pass-authz-integration/pom.xml:205:                  <container>elasticsearch</container>
./pass-authz-integration/pom.xml:229:                  <PASS_ELASTICSEARCH_URL>http://elasticsearch:9200</PASS_ELASTICSEARCH_URL>
./pass-authz-integration/pom.xml:263:              <alias>elasticsearch</alias>
./pass-authz-integration/pom.xml:264:              <name>docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3</name>
./pass-authz-integration/pom.xml:278:                  <alias>elasticsearch</alias>
./pass-authz-integration/src/test/java/org/dataconservancy/pass/authz/FcrepoIT.java:76:        if (System.getProperty("pass.elasticsearch.url") == null) {
./pass-authz-integration/src/test/java/org/dataconservancy/pass/authz/FcrepoIT.java:77:            System.setProperty("pass.elasticsearch.url", "http://localhost:9200/pass/");
./pass-authz-integration/src/test/java/org/dataconservancy/pass/authz/PolicyListenerIT.java:104:                .withEnv("PASS_ELASICSEARCH_URL", System.getProperty("pass.elasticsearch.url"))