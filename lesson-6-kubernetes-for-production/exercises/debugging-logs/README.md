# Overview

This is a simple NodeJS + ExpressJS project that is designed to simulate output for what logs may look like. The file `make_requests.sh` is set up to programatically make API requests.

## Local Setup

**_Note_**: This is only needed if you want to run the app locally. You don't need to install the dependencies or run the server if you are running the code inside a Docker container.

- Install dependencies: `npm install`
- Run server: `node server.js`

## Usage

By default, the application should be loaded on `localhost:8080`. It should provide an HTTP 200 response when loaded at `localhost:8080/health`.

## Container Setup

- Build image: `docker build .`
- Run container with image: `docker run {image_id}` where `image_id` can be retrieved by running `docker images` and found under the column `IMAGE ID`
- You can use the `-d` flag to run the container in the background. This will enable you to run other commands in your terminal while the container is running.

## Container Teardown

- Remove container: `docker kill {container_id}` where `container_id` can be retrieved by running `docker ps` and found under the column `CONTAINER ID`

## Sample log requests

Server running on port 8080
9/15/2022, 3:51:06 PM: 02f44f89-e363-4f66-90f8-072ffce8fb0d - User justin requested for resource
9/15/2022, 3:51:06 PM: bc55808f-2fcd-4c74-b258-52359be2513a - User justin requested for resource
9/15/2022, 3:51:07 PM: be428701-6f7c-41b3-895a-65e9d99d3baa - User justin requested for resource
9/15/2022, 3:51:08 PM: d5471885-fc45-4cb2-ac12-ac7f5f94a028 - User justin requested for resource
9/15/2022, 3:51:13 PM: bc55808f-2fcd-4c74-b258-52359be2513a - Finished processing request for justin
9/15/2022, 3:51:14 PM: be428701-6f7c-41b3-895a-65e9d99d3baa - Finished processing request for justin
9/15/2022, 3:51:14 PM: 02f44f89-e363-4f66-90f8-072ffce8fb0d - Finished processing request for justin
9/15/2022, 3:51:18 PM: d5471885-fc45-4cb2-ac12-ac7f5f94a028 - Finished processing request for justin
