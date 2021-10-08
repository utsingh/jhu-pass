OA-PASS

https://github.com/OA-PASS/pass-ember


Tasks Completed
1. Docker public image build
2. Elasticsearch and kibana native install

Questions and Tasks PENDING:
1. Build docker with JHU/Harvard assets?
2. Platform overview with deployment
3. Docs / Wiki where? Git or somewhere else? Internal wiki?
4. JHU assets credentials if JHU/Harvard assets used
5. how to install elasticsearch 7 within docker and commit to image? docker image changes
6. how to remove elasticsearch 6 from docker image
7. PASS docker is slow? how can allocate more memory/cpu
8. Any other students working on this with whom I could collaborate?
9. Git and docker repository branch access and priveleges (also demo of how to push a demo branch to docker repo)
10. Emberjs experiment?

Obervations / ERRORS
1. Logout not working on staff1 (404 not found pass.local/logout) -- working on pass.jhu.edu
2. Login button disappeared after login. No logout option on pass.local
3. Acceptance Errors on tests? https://pass.local/app/tests

Documentation message not reached:
Wait for the containers to finish coming up, this could take 5-10 minutes. There will be a long pause while the ember container builds. When you see the "Build successful" message from ember and a small table listing the "Slowest Nodes" that indicates the application is ready to use. It will look similar to: