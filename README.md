# Dockerizing a React app

A template for a development and production ready dockerized React application. 

The Dockerfile.dev includes volumes for hot reloading. The docker-compose.yml file is also only used for development- it runs the react server as well as test server.

The production ready Dockerfile includes nginx to serve up static content.

To run the dev server: `docker-compose up --build`

To run in production:
```
docker build -t sample-app .
docker run -p 8080:80 sample-app
```

Files added on top of create-react-app:
- .dockerignore
- Dockerfile.dev
- docker-compose.yml
- Dockerfile

Travis CI is used to build a CI/CD pipeline, along with AWS Elastic Beanstalk.
