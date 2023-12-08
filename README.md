# docker-compose-challenge

### Create a simple, mock API in the `docker-compose.yaml` file

1. Setup an haproxy container as the API "front door". Configure haproxy to start on port 8100. Expose port 8100 to the host.
2. Setup a mock API cluster using the `nginxdemos/hello` Docker image. Make sure there are 3 instances of `nginxdemos/hello` running.
3. Modify the haproxy config to route `/api` to the API cluster. It should load balance across the 3 instances.

### Outcome

- Start everything by running `docker-compose up` in the directory of the `docker-compose.yaml` file
- In the browser, go to http://localhost:8100/api
- As you click the browser refresh, observe the "Server name" cycling through the 3 backend instances.

Example:

<img width="561" alt="Screenshot 2023-12-08 at 5 39 08 PM (2)" src="https://github.com/flex-rental-solutions/docker-compose-challenge/assets/192500/1821ab62-1396-4770-bce7-bdfe4f2744f5">
