
# EchoVibe

## Introduction

Welcome to the EchoVibe documentation! This document provides an overview of the social media app backend, including its architecture, components, and usage. The app allows users to manage and track their tasks.
## Project Overview

The app is a web-based problem solving application built using Node.js, Express.js, and MongoDB. It provides the following key features:

- User registration and login.
- Posting problems along with their code and tags(if necessary)
- Post retrieval for authenticated users.
- Load balancing .
- Answers to the task can be told in comments with code.


## Installation

To run the TODO app locally, follow these installation steps:

### Prerequisites

- Node.js and npm installed.
- MongoDB installed and running.

### Installation Steps

1. Clone the project repository.
2. Install project dependencies.(`npm install`)
3. Set up environment variables by creating a `.env` file.
4. Start the application. (`node index.js`)

## Configuration

The app uses environment variables for configuration. Make sure to set the necessary environment variables in the `.env` file for your specific environment.

## API Endpoints

### User Routes

- **POST /user/signup**: Register a new user with a unique username and hashed password.
- **POST /user/login**: Authenticate a user based on their username and password, providing an access token upon successful login.

### Task Routes

- **POST /post/upload**: Upload a new post.
- **GET /post/allposts:**: Retrieve all posts.

- **GET /post/:id**: Retrieve a specific post by its ID.
- **GET /post/user/all**: Retrieve all posts by a specific user.
- **GET /post/like/:id**: Like a post .
- **POST /post/comment/:id**:Comment on a post.
- **POST /post/follow/:iden**:  Follow a user.

## Models

### User Model

- **username**: A unique string representing the user's username.
- **password**: A hashed string representing the user's password.
- **name**: A string representing the user's name.
- **posts**: An array of references to Task documents.
- **followers**: An array of users following.
- **following**: An array of users the logged in user follows.
### Task Model

- **tweet**:A basis message or query send by the user.
- **owner**: A string representing the title or name of the user.
- **code**: A string providing a description of the code problem.
- **title**: A string field describing the title of the problem.
- **tags**: An array of subtopics related to that problem.
- **likes**: An array of users who liked the post.
- **answers**: An array of users who commented on that post .
- **createdAt**: A date field representing the time of task creation.



## Middleware

### Authentication Middleware

- **authenticateToken**: Verify JWT tokens in request headers to authenticate users for protected routes.






## deployed link : https://echovibe.onrender.com
