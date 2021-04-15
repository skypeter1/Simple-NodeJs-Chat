## Simple Websocket chat App

This is a simple chat app using nodejs, socket.io, websockets and CloudFoundry


### Run Localy

Go to the source directory and type:

`npm install` 

and then go to the app.js file directory

`node app.js`

Go to your localhost

http://localhost:8080/


### Deploy to cloud Foundry

You'll need to have the cf-cli installed for this

Log into your space

`cf login -a <endpoint> -u <user> -o <org> -s <space>`

From the rrot directory push your app to

`cf push -f manifest.yml`

Have fun :)