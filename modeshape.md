./index-providers/pom.xml:87:        <module>modeshape-elasticsearch-index-provider</module>      
./index-providers/modeshape-elasticsearch-index-provider/pom.xml:11:    <artifactId>modeshape-elasticsearch-index-provider</artifactId>
./index-providers/modeshape-elasticsearch-index-provider/pom.xml:13:    <name>ModeShape Elasticsearch Index Provider</name>
./index-providers/modeshape-elasticsearch-index-provider/pom.xml:14:    <description>ModeShape index provider that uses Elasticsearch engine</description>
./index-providers/modeshape-elasticsearch-index-provider/pom.xml:22:            <groupId>org.elasticsearch</groupId>
./index-providers/modeshape-elasticsearch-index-provider/pom.xml:23:            <artifactId>elasticsearch</artifactId>
./index-providers/modeshape-elasticsearch-index-provider/src/test/resources/config/repo-config1.json:19:        "elasticsearch" : {
./index-providers/modeshape-elasticsearch-index-provider/src/test/resources/config/repo-config1.json:20:            "classname" : "elasticsearch",
./index-providers/modeshape-elasticsearch-index-provider/src/test/resources/log4j.properties:17:log4j.logger.org.elasticsearch=WARN
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/EsIndexTest.java:16:package org.modeshape.jcr.index.elasticsearch;
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/EsIndexTest.java:26:import org.elasticsearch.common.settings.Settings;
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/EsIndexTest.java:27:import org.elasticsearch.node.Node;
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/EsIndexTest.java:28:import org.elasticsearch.node.NodeBuilder;
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/EsIndexTest.java:36:import org.modeshape.jcr.index.elasticsearch.client.EsClient;
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/EsIndexProviderTest.java:16:package org.modeshape.jcr.index.elasticsearch;
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/EsIndexProviderTest.java:21:import org.elasticsearch.common.settings.Settings;
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/EsIndexProviderTest.java:22:import org.elasticsearch.node.NodeBuilder;
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/EsIndexProviderTest.java:42:    private static org.elasticsearch.node.Node esNode;
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/EsIndexProviderTest.java:54:        //configure Elasticsearch node
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/EsIndexProviderTest.java:93:        return "elasticsearch";
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/client/EsClientTest.java:16:package org.modeshape.jcr.index.elasticsearch.client;
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/client/EsClientTest.java:19:import org.elasticsearch.common.settings.Settings;
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/client/EsClientTest.java:20:import org.elasticsearch.node.Node;
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/client/EsClientTest.java:21:import org.elasticsearch.node.NodeBuilder;
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/client/EsClientTest.java:31:import org.modeshape.jcr.index.elasticsearch.EsIndexColumn;
./index-providers/modeshape-elasticsearch-index-provider/src/test/java/org/modeshape/jcr/index/elasticsearch/client/EsClientTest.java:32:import org.modeshape.jcr.index.elasticsearch.EsIndexColumns;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/Operations.java:16:package org.modeshape.jcr.index.elasticsearch;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/Operations.java:38:import org.modeshape.jcr.index.elasticsearch.client.EsRequest;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/Operations.java:39:import org.modeshape.jcr.index.elasticsearch.query.AndQuery;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/Operations.java:40:import org.modeshape.jcr.index.elasticsearch.query.BoolQuery;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/Operations.java:41:import org.modeshape.jcr.index.elasticsearch.query.ExistsQuery;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/Operations.java:42:import org.modeshape.jcr.index.elasticsearch.query.MatchAllQuery;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/Operations.java:43:import org.modeshape.jcr.index.elasticsearch.query.MatchQuery;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/Operations.java:44:import org.modeshape.jcr.index.elasticsearch.query.NotQuery;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/Operations.java:45:import org.modeshape.jcr.index.elasticsearch.query.OrQuery;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/Operations.java:46:import org.modeshape.jcr.index.elasticsearch.query.Query;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/Operations.java:47:import org.modeshape.jcr.index.elasticsearch.query.RangeQuery;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/Operations.java:48:import org.modeshape.jcr.index.elasticsearch.query.StringQuery;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/Operations.java:49:import org.modeshape.jcr.index.elasticsearch.query.TermsQuery;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/Operations.java:50:import org.modeshape.jcr.index.elasticsearch.query.WildcardQuery;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndexProvider.java:16:package org.modeshape.jcr.index.elasticsearch;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndexProvider.java:24:import org.modeshape.jcr.index.elasticsearch.client.EsClient;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndexProvider.java:51:        logger().debug("Elasticsearch index provider for repository '{0}' "
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndexProvider.java:94:        logger().debug("Shutting down the elasticsearch index provider '{0}' in repository '{1}'", getName(), getRepositoryName());
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndex.java:16:package org.modeshape.jcr.index.elasticsearch;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndex.java:25:import org.modeshape.jcr.index.elasticsearch.client.EsClient;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndex.java:26:import org.modeshape.jcr.index.elasticsearch.client.EsRequest;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndex.java:31: * Index stored in Elasticsearch.
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndex.java:46:     * @param client provides access to the elasticsearch functions.
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndex.java:63:     * @param client provides access to the elasticsearch functions.
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndexColumns.java:16:package org.modeshape.jcr.index.elasticsearch;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndexColumns.java:24:import org.modeshape.jcr.index.elasticsearch.client.EsRequest;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndexColumns.java:111:     * Provides Elasticsearch mapping definition for the given type and 
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndexColumn.java:16:package org.modeshape.jcr.index.elasticsearch;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndexColumn.java:33: * Elasticsearch field definition.
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndexColumn.java:35: * Provides definition for elasticsearch field and implements value 
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndexColumn.java:109:     * between JCR type of this column and Elasticsearch core type of this column.
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndexException.java:16:package org.modeshape.jcr.index.elasticsearch;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsIndexException.java:19: * Elasticsearch index specific exception.
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/SearchResults.java:16:package org.modeshape.jcr.index.elasticsearch;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/SearchResults.java:23:import org.modeshape.jcr.index.elasticsearch.client.EsClient;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/SearchResults.java:24:import org.modeshape.jcr.index.elasticsearch.client.EsRequest;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/SearchResults.java:25:import org.modeshape.jcr.index.elasticsearch.client.EsResponse;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsManagedIndexBuilder.java:16:package org.modeshape.jcr.index.elasticsearch;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsManagedIndexBuilder.java:24:import org.modeshape.jcr.index.elasticsearch.client.EsClient;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsManagedIndexBuilder.java:30: * Index builder for Elasticsearch indexes.
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/EsManagedIndexBuilder.java:41:     * @param client interface for elasticsearch cluster.
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/WildcardQuery.java:16:package org.modeshape.jcr.index.elasticsearch.query;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/WildcardQuery.java:18:import org.modeshape.jcr.index.elasticsearch.client.EsRequest;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/RangeQuery.java:16:package org.modeshape.jcr.index.elasticsearch.query;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/RangeQuery.java:18:import org.modeshape.jcr.index.elasticsearch.client.EsRequest;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/BoolQuery.java:16:package org.modeshape.jcr.index.elasticsearch.query;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/BoolQuery.java:19:import org.modeshape.jcr.index.elasticsearch.client.EsRequest;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/MatchAllQuery.java:16:package org.modeshape.jcr.index.elasticsearch.query;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/MatchAllQuery.java:18:import org.modeshape.jcr.index.elasticsearch.client.EsRequest;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/Query.java:16:package org.modeshape.jcr.index.elasticsearch.query;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/Query.java:18:import org.modeshape.jcr.index.elasticsearch.client.EsRequest;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/AndQuery.java:16:package org.modeshape.jcr.index.elasticsearch.query;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/AndQuery.java:18:import org.modeshape.jcr.index.elasticsearch.client.EsRequest;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/ExistsQuery.java:16:package org.modeshape.jcr.index.elasticsearch.query;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/ExistsQuery.java:18:import org.modeshape.jcr.index.elasticsearch.client.EsRequest;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/TermsQuery.java:16:package org.modeshape.jcr.index.elasticsearch.query;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/TermsQuery.java:18:import org.modeshape.jcr.index.elasticsearch.client.EsRequest;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/MatchQuery.java:16:package org.modeshape.jcr.index.elasticsearch.query;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/MatchQuery.java:18:import org.modeshape.jcr.index.elasticsearch.client.EsRequest;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/NotQuery.java:16:package org.modeshape.jcr.index.elasticsearch.query;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/NotQuery.java:18:import org.modeshape.jcr.index.elasticsearch.client.EsRequest;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/StringQuery.java:16:package org.modeshape.jcr.index.elasticsearch.query;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/StringQuery.java:18:import org.modeshape.jcr.index.elasticsearch.client.EsRequest;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/OrQuery.java:16:package org.modeshape.jcr.index.elasticsearch.query;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/query/OrQuery.java:18:import org.modeshape.jcr.index.elasticsearch.client.EsRequest;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/client/EsClient.java:16:package org.modeshape.jcr.index.elasticsearch.client;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/client/EsClient.java:30:import org.modeshape.jcr.index.elasticsearch.query.MatchAllQuery;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/client/EsClient.java:33: * HTTP-based interface for the Elasticsearch engine.
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/client/EsRequest.java:16:package org.modeshape.jcr.index.elasticsearch.client;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/client/EsRequest.java:27: * Json document used for exchange data with Elasticsearch engine.
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/client/EsResponse.java:16:package org.modeshape.jcr.index.elasticsearch.client;
./index-providers/modeshape-elasticsearch-index-provider/src/main/java/org/modeshape/jcr/index/elasticsearch/client/EsResponse.java:26: * Json document used for exchange data with Elasticsearch engine.
./modeshape-distribution/pom.xml:155:            <artifactId>modeshape-elasticsearch-index-provider</artifactId>
./deploy/jbossas/kit/jboss-wf/org/modeshape/index-provider/elasticsearch/main/module.xml:18:<module xmlns="urn:jboss:module:1.3" name="org.modeshape.index-provider.elasticsearch">
./deploy/jbossas/kit/jboss-wf/org/modeshape/index-provider/elasticsearch/main/module.xml:20:        <resource-root path="modeshape-elasticsearch-index-provider-${project.version}.jar" />
./deploy/jbossas/modeshape-jbossas-subsystem/src/main/resources/org/modeshape/jboss/subsystem/modules.properties:25:org.modeshape.jcr.index.elasticsearch.EsIndexProvider = org.modeshape.index-provider.elasticsearch
./integration/modeshape-jbossas-integration-tests/pom.xml:165:        <!-- Needed by the Elasticsearch test -->
./integration/modeshape-jbossas-integration-tests/pom.xml:167:            <groupId>org.elasticsearch</groupId>
./integration/modeshape-jbossas-integration-tests/pom.xml:168:            <artifactId>elasticsearch</artifactId>
./integration/modeshape-jbossas-integration-tests/src/test/assembly/es-wf-kit.xml:15:            <outputDirectory>modules/org/elasticsearch/${version.org.elasticsearch}</outputDirectory>
./integration/modeshape-jbossas-integration-tests/src/test/assembly/es-wf-kit.xml:27:                <include>org.elasticsearch</include>
./integration/modeshape-jbossas-integration-tests/src/test/assembly/es-wf-kit.xml:31:            <outputDirectory>modules/org/elasticsearch/${version.org.elasticsearch}</outputDirectory>
./integration/modeshape-jbossas-integration-tests/src/test/assembly/es-module.xml:1:<module xmlns="urn:jboss:module:1.3" name="org.elasticsearch" slot="${version.org.elasticsearch}">
./integration/modeshape-jbossas-integration-tests/src/test/assembly/es-module.xml:3:        <resource-root path="elasticsearch-${version.org.elasticsearch}.jar" />
./integration/modeshape-jbossas-integration-tests/src/test/java/org/modeshape/test/integration/EsIndexIntegrationTest.java:24:import org.elasticsearch.common.settings.Settings;
./integration/modeshape-jbossas-integration-tests/src/test/java/org/modeshape/test/integration/EsIndexIntegrationTest.java:25:import org.elasticsearch.node.NodeBuilder;
./integration/modeshape-jbossas-integration-tests/src/test/java/org/modeshape/test/integration/EsIndexIntegrationTest.java:58:    private static org.elasticsearch.node.Node esNode;
./integration/modeshape-jbossas-integration-tests/src/test/java/org/modeshape/test/integration/EsIndexIntegrationTest.java:85:        //configure Elasticsearch node
./integration/modeshape-jbossas-integration-tests/src/test/java/org/modeshape/test/integration/EsIndexIntegrationTest.java:121:    public void shouldQueryUsingElasticsearchIndex() throws Exception {
./integration/modeshape-jbossas-integration-tests/src/main/resources/standalone/configuration/standalone-modeshape.xml:593:                    <index-provider classname="elasticsearch"/> 
./integration/modeshape-jbossas-integration-tests/src/main/resources/standalone/configuration/standalone-modeshape.xml:596:                    <index name="mime-types" provider-name="elasticsearch" synchronous="true" kind="value" node-type="mix:mimeType" columns="jcr:mimeType(STRING)"/>
./integration/modeshape-jbossas-integration-tests/src/main/webapp/WEB-INF/jboss-deployment-structure.xml:5:	    <module name="org.elasticsearch" slot="${version.org.elasticsearch}" services="import" />
./modeshape-assembly-descriptors/src/main/resources/assemblies/jboss-wf-dist.xml:410:            <outputDirectory>modules/org/modeshape/index-provider/elasticsearch/main</outputDirectory>
./modeshape-assembly-descriptors/src/main/resources/assemblies/jboss-wf-dist.xml:413:                <include>org.modeshape:modeshape-elasticsearch-index-provider:jar</include>
./modeshape-assembly-descriptors/src/main/resources/assemblies/binary-distribution.xml:133:            <directory>../index-providers/modeshape-elasticsearch-index-provider/target/${binary.dist.name}</directory>
./modeshape-assembly-descriptors/src/main/resources/assemblies/binary-distribution.xml:134:            <outputDirectory>./modules/modeshape-elasticsearch-index-provider</outputDirectory>
./modeshape-parent/pom.xml:220:        <version.org.elasticsearch>2.1.0</version.org.elasticsearch>
./modeshape-parent/pom.xml:1004:                <artifactId>modeshape-elasticsearch-index-provider</artifactId>
./modeshape-parent/pom.xml:2076:               <groupId>org.elasticsearch</groupId>
./modeshape-parent/pom.xml:2077:               <artifactId>elasticsearch</artifactId>
./modeshape-parent/pom.xml:2078:               <version>${version.org.elasticsearch}</version>
Binary file ./.git/index matches
./modeshape-jcr/src/main/java/org/modeshape/jcr/RepositoryConfiguration.java:690:        aliases.put("elasticsearch", "org.modeshape.jcr.index.elasticsearch.EsIndexProvider");
