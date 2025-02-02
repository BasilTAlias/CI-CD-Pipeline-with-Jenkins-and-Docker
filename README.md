# CI/CD Pipeline with Jenkins and Docker

This project demonstrates a CI/CD pipeline using Jenkins and Docker. The pipeline automates the process of deploying a website using a Docker container.

## Overview

- **Jenkins Server**: Used for continuous integration and deployment.
- **Docker Server**: Used to containerize the website and serve it using Nginx.

## Prerequisites

- Two EC2 instances (one for Jenkins and one for Docker)
- Jenkins installed on one EC2 instance
- Docker installed on the other EC2 instance
- GitHub repository to store the website files

## Architecture Diagram

![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/1.png)

$~$

---

## Steps to Set Up the CI/CD Pipeline

### 1. Provisioned Two EC2 Instances
   - Two EC2 instances were created: one for Jenkins and another for Docker.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/2.png)

---

### 2. Jenkins Installation Completed
   - Jenkins was successfully installed and configured on the first EC2 instance.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/3.png)

---

### 3. Docker Installation Completed
   - Docker was successfully installed and configured on the second EC2 instance.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/4.png)

---

### 4. Website Template Downloaded
   - A website template was downloaded from [free-css.com](https://www.free-css.com/).

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/5.png)

---

### 5. Files Extracted
   - The website template files were extracted for further use.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/6.png)

---

### 6. Files Uploaded to GitHub Repository
   - The extracted files were uploaded to a GitHub repository for version control.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/7.png)

---

### 7. Jenkins Configuration and Login
   - Jenkins was configured, and the user successfully logged into the Jenkins dashboard.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/8.png)

---

### 8. Freestyle Project Created in Jenkins
   - A new freestyle project was created in Jenkins to manage the CI/CD pipeline.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/9.png)

---

### 9. GitHub Repository URL Configured
   - The GitHub repository URL was configured in the Jenkins project settings.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/10.png)

---

### 10. Branch Selected in Repository
   - The appropriate branch was selected in the Jenkins project configuration.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/11.png)

---

### 11. GitHub Hook Trigger Enabled
   - The GitHub hook trigger was enabled for GITScm polling to automate builds on code changes.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/12.png)

---

### 12. Webhooks Configured in GitHub
   - Webhooks were added in GitHub to trigger Jenkins builds on push and pull request events.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/13.png)

---

### 13. Passwordless SSH Login Configured
   - Passwordless SSH login was configured between the Jenkins server and the Docker server for seamless communication.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/14.png)

---

### 14. Successful Connection to Docker Server
   - The Jenkins server successfully established a connection to the Docker server without requiring a password.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/15.png)

---

### 15. Website Files Copied to Docker Server
   - All website files were copied to the Docker server under a dedicated `website` directory.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/16.png)
   
   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/17.png)

---

### 16. Dockerfile Created
   - A Dockerfile was created to configure an Nginx container and copy the website files to the HTML directory.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/18.png)

---

### 17. Remote Shell Configured for Docker Build
   - A remote shell was configured in Jenkins to build the Docker image and run the container, exposing the website on port 8085.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/19.png)

---

### 18. Website Successfully Accessed
   - The website was successfully accessed via the Docker server's IP address and port 8085.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/20.png)

---

### 19. Code Modified Using Visual Studio Code
   - The website code was modified and improved using Visual Studio Code.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/21.png)

---

### 20. Code Committed and Pushed to GitHub
   - The modified code was committed and pushed to the GitHub repository.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/22.png)

---

### 21. Automatic Build Triggered by Jenkins
   - Jenkins automatically triggered a build and deployment process upon detecting the new changes in the GitHub repository.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/23.png)

---

### 22. Jenkins Console Output
   - The Jenkins console output displayed the build process and deployment details.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/24.png)

---

### 23. Verified Updated Website
   - The updated website was verified to ensure the changes were successfully deployed.

   ![Alt text of the image](https://github.com/BasilTAlias/jenkins-docker/blob/main/images/readme-images/25.png)

---

## Conclusion

This CI/CD pipeline automates the deployment of a website using Jenkins and Docker. It demonstrates how to set up a continuous integration and deployment process that can be easily adapted for other projects.

---

