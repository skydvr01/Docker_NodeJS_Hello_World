This demo application shows how to serve a simple HTML file via a NodeJS http server called "http-server" and can be found here: https://www.npmjs.com/package/http-server. Note that the server defaults to port 8080. 

Step 1 -- Install NodeJS and Git -- https://nodejs.org/en/download/ && https://githowto.com/
"git clone https://github.com/skydvr01/Docker_NodeJS_Hello_World.git
Step 2 -- Open a terminal window and create a temporary directory (call it anything you want)
Step 4 -- Type "npm install" -- This will have NodeJS read the package.json file and install the necessary dependencies (http-server module in this case) 
Step 4 -- Type "npm start" -- This will start the http-server server 
Step 5 -- Press "Command" button and click the link provided. You should see this <show image> in a new browser window. Congrats! You started a webserver and served up index.html! 
Step 6 -- Type "docker image build -t test:1.0 ."
Step 7 -- Type "docker container run --publish 8090:8000 --detach test:1.0"
	+ "publish 8090:8000" -- This tells docker to forward traffic incoming on the host’s port 8090 (your computer), to the container’s port 8080 (containers have their own private set of ports, so if we want to reach one from the network, we have to forward traffic to it in this way; otherwise, firewall rules will prevent all network traffic from reaching your container, as a default security posture).
	+ "detach" --Tells Docker to run this container in the background
Step 8 -- Type "localhost:8090" into a new browser window and you should see <show image>. Congrats! You have just dockerized a webpage and served it up via NodeJS!

https://docs.npmjs.com/files/package-lock.json
https://stackoverflow.com/questions/9023672/how-do-i-resolve-cannot-find-module-error-using-node-js

Additional Goodies 
	+ Docker Getting Started Guide -- https://docs.docker.com/get-started/part2/
	+ Remove entire Linux directories -- https://www.computerhope.com/issues/ch000798.htm -- "rm -r mydir"
	+ Basic Git Commands -- https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository
	+ Using package-lock.json instead of package.json -- https://docs.npmjs.com/files/package-lock.json 
https://stackoverflow.com/questions/37744961/docker-run-vs-create
