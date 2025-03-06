Clone the repo: git clone https://github.com/Mohdsahil/node-express-backend-articture.git

Install dependencies: npm install
Node Version - v20.12.0
-------------------------------------------
Steps to start the project
1. Run npm i to install necessary dependencies
2. Navigate to directories using cd
3. Run command "npm run start" to start the project 

--------------------------------------------

add DB_URL and JWT_SECRET
PORT=3001
DB_URL=<YOUR DB URL>
JWT_SECRET=<YOUR SECRET>
BASE_URL=http://localhost:3001

```
start backend: npm run start
```
# docker-task
Build and Run the Docker Images:

After creating the Dockerfiles, build and run the Docker images for each microservice:
docker build -t service1-image .

Run the Docker Container:
docker run -p 3001:3001 service1-image

Verify the Microservices:
curl http://localhost:3001

To manage all microservices simultaneously, Create a docker-compose.yml file in the root directory:
docker-compose up
