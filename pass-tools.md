./cmd/pass-tools/main.go:41:			Name:        "es, pass.elasticsearch.url",
./cmd/pass-tools/main.go:42:			Usage:       "Elasticsearch URL",
./cmd/pass-tools/main.go:43:			EnvVar:      "PASS_ELASTICSEARCH_URL",
./README.md:49:Fedora and elasticsearch parameters are described in the `pass-tools -h` help:
./README.md:67:       --es value, --pass.elasticsearch.url value                Elasticsearch URL (default: "http://localhost:9200/pass/_search") [$PASS_ELASTICSEARCH_URL]
./README.md:73:Notice that Fedora and elasticsearch connection parameters are global options, have default values, and can be defined by environment variables as described in the help.
./README.md:150:For integration tests, you need to have Fedora and Elasticsearch running.  Use the provided `docker-compose` file to do that
./lib/assign/grant.go:117:	}, resultsPtr), "elasticsearch query for %s ($%s = %s) failed", t, key, field)
./lib/es/query.go:8:// QueryMatch creates an elasticsearch match query from the given terms
./lib/es/result.go:9:// IDResults encapsulates an elasticsearch results containing matching entity IDs.
./lib/es/result.go:21:// GrantResults encapsulates elasticsearch results containing matching grants
./lib/es/result.go:31:// SubmissionResults encapsulates elasticsearch results containing matching submissions
./lib/client/client.go:34:// Simple PASS client for hitting a server (Fedora, Elasticsearch, etc)