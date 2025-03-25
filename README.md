# CI/CD Pipeline for Building and Publishing Docker Images

[![CI/CD](https://github.com/Alexander77063/cicd-build-docker-image/actions/workflows/main.yml/badge.svg)](https://github.com/Alexander77063/cicd-build-docker-image/actions/workflows/main.yml)

A GitHub Actions workflow example for automatically building and pushing Docker images to Docker Hub.

## 📝 Description

This repository demonstrates a CI/CD pipeline that automatically:
- Builds a Docker image on code changes
- Tags the image with the Git commit SHA
- Pushes the image to Docker Hub
- Runs on every push to the `main` branch and pull requests

## 🚀 Features

- Automated Docker image builds on push events
- Image tagging with commit references for traceability
- Docker Hub integration for image publishing
- GitHub Actions workflow validation on pull requests
- Simple example Dockerfile with Nginx server

## ⚙️ Prerequisites

- Docker Hub account
- GitHub repository
- Basic understanding of GitHub Actions
- Docker installed locally (for development)

## 🛠️ Usage

1. **Fork/clone** this repository
2. **Create Docker Hub secrets** in your GitHub repository:
   - `DOCKERHUB_USERNAME` - Your Docker Hub username
   - `DOCKERHUB_TOKEN` - Your Docker Hub access token
3. **Modify** the following in `.github/workflows/main.yml`:
   ```yaml
   env:
     DOCKERHUB_USERNAME: ${{ secrets.DOCKERHUB_USERNAME }}
     IMAGE_NAME: your-image-name  # Change this
4. Push changes to trigger the workflow
