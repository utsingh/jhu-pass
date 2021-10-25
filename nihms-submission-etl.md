./nihms-etl-integration/pom.xml:112:                  <PI_ES_BASE>http://elasticsearch:9200/</PI_ES_BASE>
./nihms-etl-integration/pom.xml:113:                  <PI_ES_INDEX>http://elasticsearch:9200/pass/</PI_ES_INDEX>
./nihms-etl-integration/pom.xml:122:                  <link>elasticsearch</link>
./nihms-etl-integration/pom.xml:136:              <alias>elasticsearch</alias>
./nihms-etl-integration/pom.xml:137:              <name>docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.3</name>
./nihms-etl-integration/pom.xml:151:                  <alias>elasticsearch</alias>
./nihms-etl-integration/pom.xml:188:            <pass.elasticsearch.url>http://${ES_HOST}:${ES_PORT}</pass.elasticsearch.url>
./nihms-etl-integration/src/test/resources/nihms-loader.properties:8:#elasticsearch properties
./nihms-etl-integration/src/test/resources/nihms-loader.properties:9:pass.elasticsearch.url=http://localhost:9200/pass
./nihms-etl-integration/src/test/resources/nihms-loader.properties:10:#pass.elasticsearch.limit= 200
./nihms-etl-integration/src/test/java/org/dataconservancy/pass/loader/nihms/integration/NihmsSubmissionEtlITBase.java:90:        if (System.getProperty("pass.elasticsearch.url") == null) {
./nihms-etl-integration/src/test/java/org/dataconservancy/pass/loader/nihms/integration/NihmsSubmissionEtlITBase.java:91:            System.setProperty("pass.elasticsearch.url", "http://localhost:9200/pass/");
./nihms-pass-client/src/test/java/org/dataconservancy/pass/client/nihms/NihmsPassClientServiceTest.java:242:        //check it doesnt pull from elasticsearch the second time
./README.md:127:pass.elasticsearch.url=http://localhost:9200/ (default value)
./README.md:129:pass.elasticsearch.limit=200
./README.md:139:* `pass.elasticsearch.url` - Base URL for elasticsearch host
./README.md:140:* `pass.elasticsearch.indices` - Index target for elasticsearch
./README.md:141:* `pass.elasticsearch.limit` - Maximum number of results to return in an Elasticsearch query. This is optional, it defaults to 200 and typically will not need to be overridden.
./nihms-data-transform-load-cli/src/main/java/org/dataconservancy/pass/loader/nihms/cli/NihmsTransformLoadApp.java:48:                                                       "pass.fedora.baseurl", "pass.elasticsearch.url",
./nihms-data-transform-load-cli/src/main/java/org/dataconservancy/pass/loader/nihms/cli/NihmsTransformLoadApp.java:49:                                                       "pass.elasticsearch.limit", "nihmsetl.data.dir",
