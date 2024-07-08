# RETH Docker Compose Visualization

This diagram visualizes the services, volumes, and network interactions defined in the RETH (Rust Ethereum) Docker Compose file.

## About the Diagram

This visualization was generated as part of an Operating Systems extra credit assignment to analyze the RETH Docker Compose file. The diagram details:

* Services provisioned
* Images used
* Data volumes created
* Network ports used
* Interactions between services, their data stores, and network ports

### How It Was Created

Instead of manually charting a block diagram, I used an automated tool to generate this visualization directly from the Docker Compose file. The process was as follows:
1. I searched for a tool to convert a Docker Compose file to a block diagram.
2. I found the docker-compose-viz tool on GitHub.
3. I used the following Docker command to generate the diagram:
```
docker run --rm -it --name dcv -v /path/to/compose/file:/input pmsipilot/docker-compose-viz render -m image --force docker-compose.yml --output-file=topology.png
```
This approach allowed for an efficient and accurate representation of the Docker Compose configuration, eliminating the need for manual diagramming and reducing the potential for errors.

### Diagram Explanation

The diagram shows:

* Services: reth, grafana, prometheus
* Volumes: Named volumes for various data stores
* Network ports: 3000, 9090, 8545, 8551, 30303, 9001
* Interactions: Visualized by lines connecting services and their associated volumes and ports

This visualization provides a clear overview of the RETH stack architecture and how its components interact within the Docker environment.

