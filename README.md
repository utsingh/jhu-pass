OA-PASS

https://github.com/OA-PASS/pass-ember


Tasks Completed
1. Docker public image build
2. Elasticsearch and kibana native install

Questions and Tasks PENDING:
1. WHERE IS ELASTICSEARCH LOCATED WITHIN GIT?
2. Build docker with JHU/Harvard assets?
3. Platform overview with deployment
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