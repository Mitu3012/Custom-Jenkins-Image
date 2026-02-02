# Custom Jenkins CI Setup using Docker & Docker Compose

This project demonstrates how to set up a **custom Jenkins Continuous Integration (CI) environment** using **Docker and Docker Compose**, with Jenkins configured to build and run Docker containers as part of CI pipelines.

The setup enables Jenkins to access Docker and Docker Compose on the host system, allowing container-based builds, deployments, and health checks.

---

## Tech Stack
- Linux
- Docker
- Docker Compose
- Jenkins
- Git

---

## Project Overview
In this project:
- Jenkins runs inside a Docker container
- A **custom Jenkins image** is built with Docker and Docker Compose installed
- Jenkins is granted access to the host Docker daemon
- Jenkins pipelines can build images, run containers, and perform health checks

This setup simulates a **real-world self-hosted CI environment**.

---

## CI Capabilities

With this setup, Jenkins pipelines can:

Build Docker images

Run Docker Compose services

Perform container health checks

Clean up containers after builds

This Jenkins instance can be reused for multiple CI projects.

## Security Note

Mounting the Docker socket gives Jenkins full control over the host Docker daemon.

This approach is common in CI environments but should be:

Restricted to trusted pipelines

Used carefully in production systems
