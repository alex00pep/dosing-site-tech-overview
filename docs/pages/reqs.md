## Features

### API Server Backend
1. User Registration
2. Authentication using JWT and OAuth "password flow" using PyJWT
2. JSON-Web-Token based authentication
3. Writing & modifying user data on the database.
4. Backend API endpoints for general and to support CRUD operations
5. Manage patients and users.
6. Calculate pellets dose based on scientific data and algorithm (business logic)
7. Security
6. 


### ReactJS Frontend
The single-page-application frontend will be developed in Javascript using React JS. The frontend will have the following components -

1. Routing using React Router
2. Login component
3. Register component
4. State management using Recoil. (Recoil is kinda cool. Check it out.)
5. Admin Dashboard
6. Higher Order Components (privateroute)
7. Utility functions and higher-order components for handling authentication


The login, register & endpoint handler component will call the API we built earlier. The login & register component will POST request the API which will return the JSON Web token to make authenticated calls to the other endpoints. The app state is just an authentication flag & user data for now. The example handler will check the auth flag before calling our API.

The frontend code will also be deployed on a docker container. We’ll use the basic Nginx image. The react code will sit behind an nginx server. The nginx server will also handle the API requests at /api and redirect them to the API server. 

### Persistent Storage
The user and patient data will be stored on a Postgres database. For now, we will just store the user’s and doctor's email and password. The patient table will have more data stored. The easiest way to get postgres on production environment use a Docker image.

## Non-functional requirements
1. Deploy using Docker Compose
Docker-Compose is an awesome tool that can handle multiple container deployments on the same host. We are creating 3 different containers for the 3 services (api, web, db) which will run on the same host machine. All we need is to create the docker-compose.yaml file.
2. Use FastAPI as backend api technology.
3. Use ReactJS as frontend technology.
4. Alembic for database migrations
5. PostgreSQL as relational database management system.
4. Deployment on Deta for FastAPI backend API and Netlify for frontend UI.

## Dependencies
React v18.1.0
Create React App v5.0.1
Node v18.2.0
npm v8.9.0
npx v8.9.0
FastAPI v0.78.0
Python v3.10


## Development Philosophy
We'll start by scaffolding a new React app with the Create React App CLI before building the backend RESTful API with FastAPI. Finally, we'll develop the backend routes along with the frontend, React components.
