# jenkins-case-study - CI/CD Pipeline using Jenkins Docker and git workflow
# 🎯 Objective:
Implement a Git Workflow.

Trigger code build automatically when committing to:

   - master → Build and publish to port 82.

   - develop → Just build, do not publish.

Create a CI/CD pipeline in Jenkins.

Build a Docker container with Ubuntu and Apache and serve the content from: /var/www/html

# Prerequisites Setup
Make sure the following are installed and configured:

Jenkins (version 2.3+)

Docker installed on Jenkins server

GitHub Webhook configured

Firewall allows port 82

# Steps
**Step 1:** Install Jenkins Over Master Machine & Create One Slave machine on AWS EC2 Instance.

**Step 2:** Fork & clone the given repository to the "Jenkins-Master" machine: https://github.com/hshar/website.git

**Step 3:** Set up the Jenkins Dashboard & Create One Node as "Slave" here.

**Step 4:** Create a “Develop” Branch & Push it into the “GitHub” Repository

**Step 5:** Install Docker Over Jenkins-Master Machine to Implement the Jenkins Pipeline

**Step 6:** Create & Configure GitHub Webhook for Trigger the Jobs

**Step 7:** Create a Dockerfile & Push it into the “Master” Branch

**Step 8:** Create Jenkins Pipeline Job and write the Jenkins Pipeline Script

**Step 9:** Trigger Pipeline Automatically
✅ Enable Webhook in GitHub

**Step 10:** Test the Pipeline
🔥 Test Case 1: Push to Master
Make a commit to the master branch.

The pipeline should:

  - Build the Docker image.

  - Publish the website on port 82.

🔥 Test Case 2: Push to Develop
Make a commit to the develop branch.

The pipeline should:

  - Build the Docker image.

  - Skip the publishing step.



**Step 11:** Access the Published Website
After pushing code to the master branch, open: http://<jenkins_server_ip>:82
