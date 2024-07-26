# Go Web Application

This is a simple website written in Golang. It uses the `net/http` package to serve HTTP requests.

## Running the server

To run the server, execute the following command:

```bash
go run main.go
```

The server will start on port 8080. You can access it by navigating to `http://localhost:8080/courses` in your web browser.

## Looks like this

![Website](static/images/golang-website.png)

--------------------------------------------------------------------------------------------------------------------
# CI/CD Pipeline for Golang Application

![DevOps](https://github.com/user-attachments/assets/b43a6d4f-2e04-46d4-a047-8346ebc4d834)


## Project Overview
This project implements a CI/CD pipeline for a Golang application using GitHub Actions and ArgoCD. The pipeline handles building, testing, and deploying the application to Azure Kubernetes Service (AKS).

## Pipeline Stages

1. **Build**
- **Objective:** Compile the Golang application.
- **Actions:**
  - Checkout the repository.
  - Set up the Go environment.
  - Build the application.

2. **Code Quality**
- **Objective:** Ensure the code adheres to quality standards.
- **Actions:**
   - Checkout the repository.
   - Run golangci-lint to perform static analysis on the code.

3. **Push**
- **Objective:** Build and push the Docker image to DockerHub.
- **Actions:**
   - Checkout the repository.
   - Set up Docker Buildx.
   - Log in to DockerHub.
   - Build and push the Docker image with a tag corresponding to the current GitHub run ID.
4. **Update Helm Chart Tag**
- **Objective:** Update the Helm chart with the new Docker image tag.
- **Actions:**
   - Checkout the repository.
   - Update the image tag in the Helm chart values file.
   - Commit and push the changes to the repository.
## Deployment
The application is deployed to AKS using ArgoCD, which ensures continuous delivery by synchronizing the desired state specified in the Helm chart with the actual state in the Kubernetes cluster.

## Conclusion
This CI/CD pipeline automates the build, test, and deployment processes for the Golang application, ensuring a streamlined and efficient workflow. By integrating GitHub Actions and ArgoCD, the project achieves robust continuous integration and continuous delivery to Azure Kubernetes Service.

--------------------------------------------------------------------------------------------------------------------
# I also wrote a blog on the project for anyone who wants to implement it.
### Blog Link: https://rohitexplainstech.hashnode.dev/go-web-app-cicd
### Linkedin: https://www.linkedin.com/in/rohitdeore/
