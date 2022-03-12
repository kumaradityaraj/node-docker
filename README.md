# NODE APP

------------

### Created a node app along with implementing DevOps best practices.

------------

- Our **node app** is a simple application of registering a user and posting.
- The user's password is **hashed**.
- **Docker** is used to create an image of the application.
- There is one **Dockerfile** and four **Docker-compose** files:-
   - **docker-compose.backup**
   - **docker-compose.dev**
   - **docker-compose.prod**
   - **docker-compose**
- Docker compose backup file is for the purpose that if our app crashes in the production mode then we can directly start the basic level of app from this file.
- Docker compose dev file is used for development purpose where the developer can create and test the code.
- Docker compose prod file is used for deploying the app in production mode.
- **Redis** database is used for storing user session.
- **Nginx** is used for load balancing.
- **Docker compose order** is maintained as our app is dependent on mongo service so if we start our app then docker checks that mongo service is up or not if not then it will start the mongo service first then our app starts.
- The **environment variables** are exported to the **aws ec2** machine.
- **WatchTower** is used for automatically pulling the image from docker hub if new code is pushed to it and starting our container by pulling the new image.
- If we push a new image to docker hub then at a time 2 containers are only updated so that our service is not down this is called **Parallelism**.
- **Docker Swarm** is used for **Orchestration**

------------
### GITFLOW

![](https://github.com/kumaradityaraj/node-docker/blob/main/Screenshot%20from%202022-03-12%2010-07-31.png)

### Docker Compose

![](https://github.com/kumaradityaraj/node-docker/blob/main/Screenshot%20from%202022-03-12%2010-08-34.png)

### Load Balancing

![](https://github.com/kumaradityaraj/node-docker/blob/main/Screenshot%20from%202022-03-12%2010-29-52.png)

#### DockerHub Image
**`docker push kumaradityaraj/node-app:tagname`**
