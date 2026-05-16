# Docker Setup

This repository contains Docker configurations for multiple applications.

## Project Structure

- **Dockerfile** - Main Nginx web server serving static HTML
- **python-app/** - Python HTTP server application
- **script-app/** - Bash script application
- **.github/workflows/** - GitHub Actions CI/CD workflows

## Applications

### 1. Nginx Web Server
Serves a static HTML page on port 80.

**Build:**
```bash
docker build -t my-nginx:latest .
```

**Run:**
```bash
docker run -p 80:8080 my-nginx:latest
```

### 2. Python App
HTTP server returning JSON responses on port 8000.

**Build:**
```bash
docker build -t my-python-app:latest ./python-app
```

**Run:**
```bash
docker run -p 8000:8000 my-python-app:latest
```

### 3. Script App
Bash script that displays hello message and current date.

**Build:**
```bash
docker build -t my-script-app:latest ./script-app
```

**Run:**
```bash
docker run my-script-app:latest
```

## CI/CD

This repository uses GitHub Actions for automated builds:
- **hello.yml** - Basic workflow that runs on push events
- **docker-build.yml** - Builds and pushes the script app image to Docker Hub

## Getting Started

1. Clone the repository
2. Build any of the applications using the commands above
3. Run the container to test locally

## Requirements

- Docker
- Docker Hub account (for pushing images)
