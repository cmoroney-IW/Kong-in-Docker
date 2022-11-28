## Installation Instructions

- Clone the repository from GitHub
- Open a terminal in the repository directory and type `docker-compose up`
- The docker container with Kong installed should now be running

## Testing Instructions

- Open a browser and enter `localhost:8002`; this should open the Kong Manager dashboard
- Scroll down and click on the default Workspace
- On the left-hand side click Services underneath API Gateway, and then click New Service
- Under Name type `test`, and under URL type `https://httpbin.org/anything`, and then click Create
- On the left-hand side click Routes, and then click New Route
- Under Service click the box and then click test
- Scroll down to Path(s), click + Add Path, type /test and then click Create
- Open a new tab in your browser and type `localhost:8000/test`
- This should return JSON data from httpbin, indicating the the service and route are working correctly
