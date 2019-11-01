This demo application shows how to serve a simple HTML file via a NodeJS http server called "http-server" and can be found here: https://www.npmjs.com/package/http-server. Note that the server defaults to port 8080. 

Step 1 -- Install NodeJS -- https://nodejs.org/en/download/
Step 2 -- Download the sample code -- 





docker container run --publish 8090:8000 --detach nodejstest:1.0
	+ "publish 8090:8000" -- This tells docker to forward traffic incoming on the host’s port 8090 (your computer), to the container’s port 8080 (containers have their own private set of ports, so if we want to reach one from the network, we have to forward traffic to it in this way; otherwise, firewall rules will prevent all network traffic from reaching your container, as a default security posture).
	+ "detach" --Tells Docker to run this container in the background


https://docs.npmjs.com/files/package-lock.json
https://stackoverflow.com/questions/9023672/how-do-i-resolve-cannot-find-module-error-using-node-js