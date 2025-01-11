--- 
# ⭐Local Elasticsearch & Kibana Setup
This project provides a local development environment for running a single-node Elasticsearch instance with Kibana, 
using Docker and Docker Compose.

--- 

## 🛠️Features
- **Single-node Elasticsearch setup for development and testing.**
- **Integrated Kibana for data visualization and monitoring.**
- **Persistent data storage using Docker volumes.**
- **Simple configuration files for Elasticsearch and Kibana.**

--- 

## 🚀Getting Started
### Prerequisites
- Docker  (version 20.x or later)
- Docker Compose (version 2.x or later)

---

## Installation
1. Clone the repository
```shell
git clone https://github.com/yourusername/localelasticsearch.git
cd localelasticsearch
```

2. Start the services
```shell
docker-compose up -d
```

3. Access the services:
- **Elasticsearch**: http://localhost:9200
- **Kibana**: http://localhost:5601

---

# 📃Project Structure
```shell
localelasticsearch/
├── docker-compose.yml       # Docker Compose file to orchestrate services
├── elasticsearch.yml        # Elasticsearch configuration
├── kibana.yml               # Kibana configuration
└── README.md                # Project documentation
```
---

# ⚙️Configurations
## Elasticsearch
- **HTTP Port**: 9200
- **Transport Port**: 9300
- **Data Directory**: es_data (mounted as a Docker volume)
- **Config file**: elasticsearch.yml

## Kibana
- **HTTP Port**: 5601
- **Connected to the Elasticsearch instance**
- **Config file**: kibana.yml

---

# 🌟 Notes
- Security is disabled (xpack.security.enabled: false) for simplicity. Do not use this setup in production.
- Ensure that ports 9200 and 5601 are not in use by other services on your machine.

---