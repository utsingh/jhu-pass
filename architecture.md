# architecture.md

The following modules deal with the ElasticSearch implementation across teh OA-Pass repository.

<flowchart.png>
                                                   
- data-model-migration.md
- deposit-services.md
- jhu-package-providers.md
- pass-docker.md
- pass-indexer.md
- pass-tools.md
- pass-doi-service.md
- nihms-submission-etl.md
- ember-fedora-adapter-store.query.md                                
- ember-fedora-adapter.md
- notification-services.md
- pass-ember.md
- java-fedora-client.md
- pass-authz.md
- pass-grant-loader.md

## java-fedora-client
* implements the java libraries for managing elastic search queries on the backend. *

1. Pass Data Client
*Creates instances of objects needed to perform PassClient requirements, and redirects to appropriate service (Index client or CRUD client).*

methods implemented:
- findByAttribute: takes in modelClass, sttribute, and value.
- findAllByAttribute: takes in modelClass, sttribute, and value.
- overloaded findAllByAttribute: takes in modelClass, attribute, value, limit, offset.
- multi-sttributes findAllByAttributes: takes in modelClass, valueAttributesMap.
- overloaded findAllByAttributes: takes in modelClass, valueAttributesMap, limit, offset.

Retrieve Search Results from ElasticSearch: getIndexerResults(String querystring, int limit, int offset)
Search the index using querystring: {}, with limit {} and offset {}", querystring,  limit, offset)

2. PASS Client API
* Takes any PassEntity and persists it in the database, returns the URI if successful or appropriate exception if not. Note that PassEntities that are being created should have null as their ID, the URI will the the ID field when reading the resource back. *
* Takes modelObj The entity to be created *
* returns URI of new record *

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
