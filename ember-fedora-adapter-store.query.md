./tests/unit/adapters/fedora-jsonld-test.js:386:      return store.query('cow', query);
./tests/unit/adapters/fedora-jsonld-test.js:406:      return store.query('cow', query);
./tests/unit/adapters/fedora-jsonld-test.js:429:      return store.query('cow', query);
./tests/integration/fedora-jsonld-test.js:397:      return store.query('cow', query);
./tests/integration/fedora-jsonld-test.js:447:      return store.query('barn', {term: {colors: 'green'}});
./tests/integration/fedora-jsonld-test.js:454:      return store.query('barn', {term: {colors : 'green'}, size: 2});
./tests/integration/fedora-jsonld-test.js:459:      return store.query('barn', {term: {colors : 'green'}, sort: {colors: {order: 'asc', mode: 'max'}},
./tests/integration/fedora-jsonld-test.js:465:      return store.query('barn', {query: {term: {colors : 'green'}}, from: 2, size: 1, info: info});
./README.md:128:Store.query is implemented on top of Elasticsearch. Fedora must have been set up such
./README.md:160:store.query('barn', {term: {colors : 'green'}, from: 10, size: 10, info: info});
./README.md:166:store.query('barn', {query: {term: {colors : 'green'}}, from: 10, size: 10, info: info});
