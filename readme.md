This demo application shows how to serve a simple HTML file via a NodeJS http server called "http-server" and can be found here: https://www.npmjs.com/package/http-server. Note that the Node http-server server defaults to port 8080. 

Step 1 -- Install NodeJS and Git -- https://nodejs.org/en/download/ && https://githowto.com/

Step 2 -- Open a terminal window and create a temporary directory (call it anything you want)

Step 3 -- Download the sample code with Git (make sure you are in your temp directory) and then CD into the directory after downloading the github repository -- Type the following command into your terminal:
```
git clone https://github.com/skydvr01/Docker_NodeJS_Hello_World.git
```
Step 5 -- Verify that the same files you see on the Github repository webpage are the same files you see in the local directory. Your local directory should look like this: 
```
ls
```

Step 4 -- Install the necessary NodeJS dependencies (http-server module in this case) by typing the following:
```
npm install
```

Step 4 -- Type "npm start" -- This will start the http-server server 
```
npm start
```
Step 5 -- Press "Command" button and click the link provided. You should see this <show image> in a new browser window. Congrats! You started a webserver and served up index.html! 

Step 6 -- Build the docker image (don't forget the period at the end of this command!).
```
docker image build -t test:1.0 .
```
Step 7 -- Run the docker image you just created
```
docker container run --publish 8090:8000 --detach test:1.0
```
* "publish 8090:8000" -- This tells docker to forward traffic incoming on the host’s port 8090 (your computer), to the container’s port 8080 (containers have their own private set of ports, so if we want to reach one from the network, we have to forward traffic to it in this way; otherwise, firewall rules will prevent all network traffic from reaching your container, as a default security posture).
* "detach" --Tells Docker to run this container in the background so that you don't have to open a new terminal window
Step 8 -- Type "localhost:8090" into a new browser window and you should see <show image>. Congrats! You have just dockerized a webpage and served it up via NodeJS!

## Good to know Docker Commands

List all running docker containers 
```
docker ps
```
Kill a specfic container 
```
docker kill <containter ID>
```
