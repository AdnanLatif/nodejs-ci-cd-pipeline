# Node.js CI/CD Pipeline with Jenkins and SonarQube

This repository contains a sample Node.js project configured for CI/CD using Jenkins and SonarQube. The setup includes Docker containers for Jenkins and SonarQube, and a Jenkins pipeline for code analysis and building Docker images.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Setup Instructions](#setup-instructions)
- [Running the Application](#running-the-application)
- [Verifying the Setup](#verifying-the-setup)
- [Jenkins Pipeline](#jenkins-pipeline)
- [SonarQube Integration](#sonarqube-integration)
- [Troubleshooting](#troubleshooting)
- [License](#license)

## Prerequisites

Before you begin, ensure you have the following installed:

1. **Docker Desktop** with WSL 2 integration enabled on Windows.
   - You can download it from [Docker's official site](https://www.docker.com/products/docker-desktop).
2. **Node.js LTS** installed on your local machine (for testing).
   - Install it from [Node.js official site](https://nodejs.org/).
3. **Git** for version control.
   - Install it from [Git's official site](https://git-scm.com/).

## Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/nodejs-ci-cd-pipeline.git
   cd nodejs-ci-cd-pipeline
   ```

Build and Start Docker Containers: Make sure you are in the project directory containing docker-compose.yml, then run:

````docker-compose up -d

Access Jenkins:

Open http://localhost:8080 in your web browser.
Retrieve the initial admin password by running:

```docker logs jenkins



### Instructions
- **Replace Placeholder Values**: Ensure to replace `yourusername` and `your-node-app-directory` with your actual GitHub username and the appropriate directory name for your Node.js application.
- **Save the File**: Save this content as `README.md` in the root of your project repository.
- **Push to GitHub**: After saving, commit your changes and push them to your GitHub repository.

If you have any additional changes or need further assistance, please let me know right away!
````
