# docker-compose-challenge

### Create a simple, mock API in the `docker-compose.yaml` file

Go to https://docs.docker.com/compose/ for more info on Docker Compose.

1. Setup an haproxy container as the API "front door". Configure haproxy to start on port 8100. Expose port 8100 to the host.
2. Setup a mock API cluster using the `nginxdemos/hello` Docker image. Make sure there are 3 instances of `nginxdemos/hello` running.
3. Modify the haproxy config to route the `/api` URL context to the API cluster and have it load balance across the 3 nginx instances.

### Outcome

- Start everything by running `docker-compose up` in the directory of the `docker-compose.yaml` file
- In the browser, go to http://localhost:8100/api
- As you click the browser refresh, observe the "Server name" cycling through the 3 backend instance id's.

**Example Browser Output**

<img width="588" alt="Screenshot 2023-12-08 at 5 42 40 PM (2)" src="https://github.com/flex-rental-solutions/docker-compose-challenge/assets/192500/f7e9ff37-f56e-4620-96d3-dab9ca331ffa">

