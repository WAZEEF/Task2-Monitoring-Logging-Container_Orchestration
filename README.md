**Monitoring & Logging Stack with Docker, Prometheus, Grafana, Loki, Promtail**

This project implements a complete observability solution for a Python microservice using containerization and open-source monitoring tools. It's built as part of an Assessment Task on Monitoring, Logging, and Container Orchestration.
Tech Stack:- Python: Sample app with health check endpoint- Docker: Containerized setup- Docker Compose: Multi-container orchestration- Prometheus: Metrics monitoring and scraping- Grafana: Dashboard visualization and alerting- Loki + Promtail: Centralized logging solution
Folder Structure: 
 .
 app/
    app.py                  # Python microservice
 Dockerfile                  # Dockerfile for Python app
 docker-compose.yml          # Compose setup for all services
 prometheus.yml              # Prometheus scrape config
 promtail-config.yml         # Promtail log shipping config
 README.md                   # You're reading it!
 Features:- Real-time service health monitoring via Prometheus- Log aggregation with Loki and Promtail- Visual dashboards in Grafana- Dockerized stack  no manual setups- Metrics exposed on /metrics endpoint
 Setup & Run:
 1. Clone the repository
 $ git clone https://github.com/WAZEEF/Task2-Monitoring-Logging-Container_Orchestration.git
 $ cd Task2-Monitoring-Logging-Container_Orchestration
 2. Start all containers
 $ docker-compose up -d
 3. Access dashboards- Grafana: http://<EC2-IP>:3000  (login: admin / admin)- Python App: http://<EC2-IP>:5000- Prometheus: http://<EC2-IP>:9090- Logs in Grafana -> Explore -> Loki -> job="dockerlogs"
 Sample Prometheus Query:
 up{job="python-app"}
 Testing:
Monitoring & Logging Stack with Docker, Prometheus, Grafana, Loki, Promtail
 $ curl http://<EC2-IP>:5000/health
 {"status": "ok"}
 License:
 MIT License  feel free to reuse and improve!
 Author:
 Wazeef Khan
 DevOps | Cloud 
 GitHub: https://github.com/WAZEEF
