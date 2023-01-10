# Containerization of a NodeJS App

## Step 1
Node is an asynchronous event driven JavaScript runtime built upon Chrome’s V8 JavaScript engine. It’s designed to build scalable network applications.
First, let’s create a simple node.js(express) application.

We are making a new directory inside the directory for currently in

#### mkdir myapp
#### cd myapp
Now, let's try to run our app in the terminal,

#### npm init
Need to enter through all of them EXCEPT this one:

#### entry point: (index.js)

Need to change this to app.js

Next

#### npm install express --save

Start text editor of choice and create a file named app.js.

#### node app.js

Our app is running now, to check, go to http://localhost:3000/

## Step 2

The next step is to create a Dockerfile.
Dockerfile — contains all the commands that are to be executed, to build an image.
We will always start from a base image, and build our own image with our app in it.
For the base image, we are going to use the official node image available in dockerhub. 
Dockerhub — where users can create their own private/public repositories to contain their images and also can access any open-source image.

## Step 3
Build the image using Dockerfile.

#### docker build -t node-app:latest .

## Step 4

Create an instance of the image (container).
We created the image, now let’s run our image.
#### docker run -p 3000:3000 node-app:latest

in this, the port 3000 from container listens in 3000 in our machine, which means we can view our application on http://localhost:3000 With this, 
now you can able to containerize your application.
