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

---------------------------------------------------------------------------------------------------------------------------------------------------------
# Screenshots

![1](https://github.com/user-attachments/assets/dfbd6cd0-025d-4a0e-a628-b4994c72bd6a)
![2](https://github.com/user-attachments/assets/1037867f-fc38-4ecc-8507-c2ce8946a4e8)
![3](https://github.com/user-attachments/assets/6bc52a48-4075-4d9f-925d-06235d8ca86d)
![4](https://github.com/user-attachments/assets/d7e5dfc1-471b-4ae7-b451-4fa57bab4022)
![5](https://github.com/user-attachments/assets/60378017-40dd-45e6-ab25-313ef7cd91e8)
![6](https://github.com/user-attachments/assets/6dd5dd34-ee53-4ec7-9a11-50d90a0859ba)
![7](https://github.com/user-attachments/assets/c8b1c895-eee5-4d7a-871e-aec3f91f93d4)
![8](https://github.com/user-attachments/assets/9988634c-42f4-48e2-9da8-0468ef919eb4)
