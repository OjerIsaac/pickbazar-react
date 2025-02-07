# **Project Setup Documentation**

## **Hosting Provider & Server Setup**

- **Hosting Provider:** [Brimble.io](https://brimble.io)
- - **Deployment Strategy:** Brimble handles deployments using **Docker containers**
- **Root Directory:** The deployment was configured to focus on `api/rest` for the REST API service.
- **Important Configuration:**  
  The root `package.json` was updated to include all workspace projects:

  ```bash
  "private": true,
  "workspaces": [
    "api/rest",
    "api/graphql",
    "admin/*",
    "shop"
  ]
  ```

## **CI/CD Pipeline Details**

- **Pipeline Managed by Brimble:**  
  Brimble automatically builds, deploys, and manages updates based on changes pushed to your GitHub repository.

## **Security Configurations Applied**

- **Environment Secrets:** All sensitive information was configured as environment variables in Brimble's dashboard.
- **HTTPS:** Brimble manages HTTPS for all deployed services.
