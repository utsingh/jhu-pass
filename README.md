# OA-PASS

URL: https://github.com/OA-PASS/pass-ember

# Meeting Recordings

### Meetings FRIDAYS 3pm.

Meeting #1 Recording: https://www.icloud.com/iclouddrive/00XNVmyign9THHb2uDukkfR5g#zoom_0

Meeting #2 Recording: 

____________________________________________________________________

# Meeting#1

## Tasks Completed
1. Docker public image build
2. Elasticsearch and kibana native install

## Questions and Tasks PENDING:
1. WHERE IS ELASTICSEARCH LOCATED WITHIN GIT?
2. Build docker with JHU/Harvard assets?
3. Platform overview with deployment. NO
4. Docs / Wiki where? Git or somewhere else? Internal wiki?
5. JHU assets credentials if JHU/Harvard assets used
6. how to install elasticsearch 7 within docker and commit to image? docker image changes
7. how to remove elasticsearch 6 from docker image
8. PASS docker is slow? how can allocate more memory/cpu
9. Any other students working on this with whom I could collaborate?
10. Git and docker repository branch access and priveleges (also demo of how to push a demo branch to docker repo)
11. Emberjs experiment?
12. java fedora client? https://github.com/OA-PASS/java-fedora-client

## Obervations / ERRORS
1. Logout not working on staff1 (404 not found pass.local/logout) -- working on pass.jhu.edu -- NO FACILITY FOR LOGOUT
2. Login button disappeared after login. No logout option on pass.local
3. Acceptance Errors on tests? https://pass.local/app/tests -- acceptance do not pass when run locally

Documentation message not reached:
Wait for the containers to finish coming up, this could take 5-10 minutes. There will be a long pause while the ember container builds. When you see the "Build successful" message from ember and a small table listing the "Slowest Nodes" that indicates the application is ready to use. It will look similar to:


## Meeting Notes with Mark and Derek:
1. ES jhu production endpoint: https://pass.jhu.edu/es
2. PASS data model: https://github.com/OA-PASS/pass-data-model
3. ES query (json also available): https://pass.jhu.edu/es?q=@type:Submission&size=20
4. PASS Ember code for Ember UI. Docker not complete stack. The complete full stack is in pass-docker. 
5. branch "minimal-assets" in https://github.com/OA-PASS/pass-docker/tree/minimal-assets should work as production equivalent version. Can develop in this if required. Eventually will need to be tested on this.
6. The full pass docker has some services which use elasticsearch that pass-ember does not have.


7. TODO inventory of everywhere elasticsearch is used AND WHAT SEARCHES IT DOES throughout the codebase. (check both pass-ember and pass-docker). (example ember user interface it does searches for submissions, user, search for grants that a auser is on, it does autocompletion on journal names;
pass-indexer writes documents to teh elastic search documents, deletes documents, updates documents, maybe something else,
java backend services deposit services searches for submissions that are ready to be submitted, grant loader services searches by award number, etc etc)

8. 3 other students working on it. are on slack.
9. assets image, jhu data in it, used in production.
10. it might get in the way that we don't have access to assets jhu.
11. Elastic search is a search appliance, clients index data, clients collect statistics. complicated history which may be asked to help with, amazon, propreitary vs open source, in production AWS service is used instead of running it yourself. ES6 used in development.
12. new features and capabilities in ES7?
13. TODO try putting a published newer ES7 image in docker compose and try with that.
14. TODO look at elasticsearch container logs and see if it complains bitterly!
15. TODO emberJS code directly makes request to teh elasticsearch endpoint. Run a UI in browser and see the requests that it is making. look through teh source code in ember version that there is a service that elasticsearch does things, configuration variable for location of elastic search endpoint, pass-ember uses anotehr ember module EMBER FEDORA ADAPTER is used by pass-ember. https://github.com/OA-PASS/ember-fedora-adapter
ember fedora adapter is  adependency in pass-ember.
16. The pass java client also queries elasticsearch https://github.com/OA-PASS/java-fedora-client
written in java / GO
17. Go through all the repositories 
18. use grep on command line to search for 
-- for javascript 
19. .env file in pass-docker. elasticsearch endpoint variable, grep for elasticsearch endpoint where in the code that is referenced.
20. for backend code, look at java fedora client and figure out which methods use elasticsearch. uses a java interface that elasticsearch provides. another level of indirection.
21. pass-indexer https://github.com/OA-PASS/pass-indexer notices which things have changed and updates elasticsearch with that.
22. new service in docker-compose to pull in kibana. change the tag for elasticsearch version TAG.
23. AWS EKS is used in production. they don't use docker compose, a seperate definition file in EKS is written. 

24. submit pull request for SOC4.


__________________________________________________________________________

# Meeting #2: Friday, October 15, 2021 3pm

## TASKS Completed

1. pass-ember upgraded to elasticsearch 7.15
2. pass-docker tried with public image (added docker-public yaml) -- FAILED
3. Question: Not sure which one is the elasticsearch variable in .env? Ask for details about modifying .env, and options for running pass-docker.
4. Share error in pass-docker deployment (with and without public image)

## TASKS PENDING
1. Documentation of elasticsearch occurences in codebase. (questions above)
2. If image issues resolved, deployment of pass-docker.
3. SHA-256 code for 7.15? Necessary?

### Exploring
1. https://www.elastic.co/guide/en/elasticsearch/reference/current/configuring-tls-docker.html

## Meeting Notes with Mark and Derek
1. docker inspect docker.elastic.co/elasticsearch/elasticsearch:7.15.1
2. update object in fedora and see how elasticsearch indexes the new object in 7.1.5
3. look through pass-ember. pass-ember does a search for grants user. pass-ember does a special auto-complete search ... etc etc
4. pass-ember is very different (javascript) is very different than batch loader (pass grants) using the fedora java client.
5. START WITH PASS-EMBER OR PASS JAVA CLIENT for documentation of where elasticsearch exists in codebase.
6. Testing the java client, minimal yaml file with repository, indexer an delasticsearch. Run tetss against it with the java client (integration tests). Then change the version of the elasticsearch and see is all tests pass. What the elasticsearch calls are, and how do i do a test on that component to make sure 
7. Documentation is next step. For each component figure out how am i going to test that it works with ES7. Most cases will have existing integration tests. Testing with ES7 will be as simple as updating the configuratioin of the integration tests to use the ES7. 
8. Integration tests, manual work looking through code. Pass integration tetss are put togetehr in maven. Poking around needed!
9. There may be the case that there arent any integration tests.
10. Code for the component that is usually unit tests, and integrtaion module for the integration tests. 
11. Start by looking through each repositories of OA-PASS. Each component is not necessarily utilized.

12. Mark DEMO: pass-ember: UI extensive use of elastic search to do different things. Dependency on ember-fedora adapter.
How javascript interacts with ES and also has integration tests in 'tests'. Description in readme file to run integration tests.
How does it use ES? app/adapters/fedora-jsonid.js Line 190 QUERY method. using elasticsearchURI .
Inside app>routes>grants>index.js when ember app visits the /grants routes, it's going to serve out a html template to user and that template is this. grantquery sorts on enddate and range, PI must be logged in user, this.store.query (each store.query will run ES).
Some magic in .env and ember config directory.

13. log in as nih-user which has 1 grant/submission keep dev tools open, open /grant and you'll see that search being run.

14. Autocomplete service: does a complicated elasticsearch query suggesting how to complete teh prefix of something. Happens when you're trying to find an existing publication.
App/services/autocomplete.js
Do a submission workflow and keep an eye on network flow in dev tools that may have hints of servcies being called. POST cna go to elasticsearch.

15. Within network > es > scroll down and look for request payload in headers.

16. Look through the code. If you have your docker compose setup properly, you can look up elastic search directly instead of through the proxy.

17. pagination is not implemented yet. We need to have the tables be paged. Note: if more search results are returned then searches only return 20 results. What happens if 21 results are found.

18. Create a document. Sections and components (populate the list from OA-pass repositories list) -- ignore the non-software repositories.
If the component does not use ES, note an dmove on.
If it does use ES, pass-indexer creates documents does not do queries. Note teh use, examples, how can i test this compoennt that it works with ES7. SOme existing integration tests, in some cases might have to manually testing. How do i do the tests has to be thought about.
How can we test everything systematically instead of manually firing up.
Do i notice any problems with how this component is using ES?

__________________________________________________________________________

# Meeting #3: Monday, Oct 25, 2021 2pm

Meeting Recording: 

## TASKS Completed

1. Systematic documentation of elasticsearch across all repos in OA-Pass
2. pass-ember, java-fedora-client, pass-docker, pass-data-model detailed docs

## Integration Testing
1. ran java-fedora-client, seems to pass all tests, still need help to make sure that assumption is correct.

## Notes
1. pass-ember: ignore everything in dist. it's compiled code of ember.
2. ember-fedora-adapter is being used within pass-ember. that adapter is using 'store.query'. run grep with that term in ember-fedora-adapter.
3. FORMAT OF SUBMISSION: name of repository, has/does not have integration tests, and these are the queries being run.
4. docker compose up -d
maven install
to get it running and then run tests with maven
5. pass-data-model make a note that index configuration is stored there
6. grant-loader has integration tests, testing interactions with fedora repository, authorized stack, etc
only interaction that grant-loader is through java-client. so no need to test it seperately.
7. check that grant-loader uses java-client. then find teh variable from java client and grep that in grant-loader and other loaders.
8. PASS is going to become a project of the eclipse foundation. reviewing some architectural decisions.

## TASKS Pending
1. Format everything better. Make an architectural diagram of elasticsearch occurences.
2. Look backwards from Java clients, loaders and download services and similar things. Ignore integration tests in repositories that are running from the java client. Find integration tests in others, and in Go client.
3. FORMAT FORMAT FORMAT!

__________________________________________________________________________

# Meeting #4: Monday, Nov 1, 2021 2:30pm

Meeting Recording: 

## Meeting notes

1. 