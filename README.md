🎡 Apache Kafka & Zookeeper Infrastructure 
📌 Project Overview
As part of my 100 Days of AI Challenge, Day 7 focuses on building the real-time data backbone required for MLOps. I have implemented a containerized Event Streaming Platform using Docker Compose, featuring a single-node Kafka broker and a Zookeeper coordinator.

🛠️ Infrastructure Stack
Orchestration: Docker Compose (Version 3.8)

Message Broker: Apache Kafka (cp-kafka:7.5.0)

Coordinator: Zookeeper (cp-zookeeper:7.5.0)

Environment: VS Code with Docker Desktop

⚙️ Configuration Highlights
Connectivity: Configured KAFKA_ADVERTISED_LISTENERS with both PLAINTEXT and PLAINTEXT_HOST to allow internal cluster traffic and external local development on port 9092.

Automation: Enabled KAFKA_AUTO_CREATE_TOPICS_ENABLE: "true" for rapid prototyping and testing of data streams.

Stability: Integrated depends_on logic to ensure Zookeeper is fully healthy before the Kafka broker attempts to initialize.