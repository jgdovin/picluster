# Docker Swarm Configurations
A collection of Docker Swarm stack configurations for deploying various applications and services. Each service configuration is organized by name, making it easy to deploy and manage stacks on your Swarm cluster.

## 🛠 Features
* Ready-to-use docker-compose.yml files for Docker Swarm mode
* Simplified directory structure for easy navigation
* Support for Raspberry Pi and ARM-based clusters
* Includes configurations for popular services and custom deployments

## 📂 Directory Structure
```
.
├── README.md                   # Documentation
├── stacks/                     # All Swarm stack configurations
│   ├── <service-name>/         # Directory for each service
│   │   └── docker-compose.yml  # Swarm stack file for the service
│   ├── nginx/                  # Example service
│   │   └── docker-compose.yml
│   ├── portainer/
│   │   └── docker-compose.yml
│   └── prometheus/
│       └── docker-compose.yml
```

## 🚀 Getting Started
### Prerequisites
* A Docker Swarm cluster (e.g., Docker Swarm mode).
* Basic knowledge of Docker Compose and stack deployment.

### Deploy a Service
1. Clone this repository:

```bash
git clone https://github.com/<your-username>/docker-swarm-configs.git
cd docker-swarm-configs
```
2. Navigate to the desired service stack:

```bash
cd stacks/<service-name>
```

### Deploy the stack:

```bash
docker stack deploy -c docker-compose.yml <stack-name>
```
### Check the status of the deployed service:

```bash
docker service ls
```

`Example: Deploying Portainer`

```bash
cd stacks/portainer
docker stack deploy -c docker-compose.yml portainer
docker service ls
```
## 🧩 Available Stacks

| Service             | Description                                   | Status  |
|---------------------|-----------------------------------------------|---------|
| **portainer**       | Docker Swarm management UI                    | ✅ Ready |
| **registry**        | Distributed image storage                     | ✅ Ready |
| **prometheus**      | Monitoring and metrics collection             | 🚧 WIP  |
| **grafana**         | Metrics visualization                         | 🚧 WIP  |
| **nginx**           | Reverse proxy and load balancer               | 🛠 Planned |
| **nextcloud**       | Self-hosted file sharing and collaboration    | 🛠 Planned |



## 🛠 Best Practices
* Ensure all services have unique stack names to avoid conflicts.
* Use Docker secrets to securely manage sensitive data.
* For ARM-based clusters, verify image compatibility with your Raspberry Pi devices.

## 📋 Contributing
Contributions are welcome! If you’d like to add or improve a configuration, feel free to submit a pull request or open an issue.

## 📄 License
This project is licensed under the MIT License. See the LICENSE file for more details.
