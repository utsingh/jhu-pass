OA-PASS

https://github.com/OA-PASS/pass-ember


FRIDAYS 3pm.

Meeting #1 Recording: https://www.icloud.com/iclouddrive/00XNVmyign9THHb2uDukkfR5g#zoom_0


Tasks Completed
1. Docker public image build
2. Elasticsearch and kibana native install

Questions and Tasks PENDING:
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

Obervations / ERRORS
1. Logout not working on staff1 (404 not found pass.local/logout) -- working on pass.jhu.edu -- NO FACILITY FOR LOGOUT
2. Login button disappeared after login. No logout option on pass.local
3. Acceptance Errors on tests? https://pass.local/app/tests -- acceptance do not pass when run locally

Documentation message not reached:
Wait for the containers to finish coming up, this could take 5-10 minutes. There will be a long pause while the ember container builds. When you see the "Build successful" message from ember and a small table listing the "Slowest Nodes" that indicates the application is ready to use. It will look similar to:



Meeting Notes with Mark:
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

Meeting #2: Friday, October 15, 2021 3pm

#TASKS Completed

1. pass-ember upgraded to elasticsearch 7.15
2. pass-docker tried with public image (added docker-public yaml) -- FAILED
3. Question: Not sure which one is the elasticsearch variable in .env? Ask for details about modifying .env, and options for running pass-docker.
4. Share error in pass-docker deployment (with and without public image)

#TASKS PENDING
1. Documentation of elasticsearch occurences in codebase. (questions above)
2. If image issues resolved, deployment of pass-docker.
3. SHA-256 code for 7.15? Necessary?

#Exploring
1. https://www.elastic.co/guide/en/elasticsearch/reference/current/configuring-tls-docker.html