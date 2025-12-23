# docker-testapp
this is our node js application in which contain html and css as a public file and there is server.js which is basically backend of our application.
* hare we are using apna collage database in server.js but there is no any database in our application so, here we are using mongo db database with the help of docker container.
* here we are going to use 2 containers one is mongo db and other is mongo express which is framework of mongo db. with the help of mongo express we can view our mongo db in web brower.
* we create these 2 container in a same docker network so they can communicate each other without external port.
* to check these database container is connected to our node js application we simply execute get request by go to localhost:5050/getUsers and in this url we see our data of users if present then our node js is connected to database.
**How to start run this node js application**
1. open code in vs code.
2. run command `node server.js` in terminal to start backend.
3. run docker compose cammand which is `docker compose -f mongodb.yaml up -d` in same path of terminal.
4. run command `docker ps` to check wheather these two container are build or not.
5. go to [link] (localhost:8081) to go to mongo express.
    1. username is admin and password is pass
    2. make some changes like create database of apanacollege-db
    3. add documents and users
6. go to [link] (localhost:5050/getUsers) to view our data in database are saved or not if it saved then our application is working.